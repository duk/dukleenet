---
layout: post
title:  "How to get Infinite Loader wth Table using React Virtualized"
date:   2017-08-01 03:53:00 -07002
categories: reactjs
---

Pulled my hair for a couple of days on this one. The key point is to use `cellDataGetter` in Column. And make sure rowData is not undefined.

{% highlight javascript %}

import React from 'react';
import ReactDOM from 'react-dom';
import { InfiniteLoader, Table, Column } from 'react-virtualized';
import 'react-virtualized/styles.css'; // only needs to be imported once

// This example assumes you have a way to know/load this information
const remoteRowCount = 10000;

const list = [];
const loadedRowsMap = [];
const STATUS_LOADING = 1;
const STATUS_LOADED = 2;

function isRowLoaded({ index }) {
  return !!loadedRowsMap[index];
}

function loadMoreRows({ startIndex, stopIndex }) {
  for (var i = startIndex; i <= stopIndex-1; i++) {
      loadedRowsMap[i] = STATUS_LOADING;
    }
  return fetch(`http://localhost:3001/users?_start=${startIndex}&_end=${stopIndex}`)
    .then(response => response.json())
    .then(json => {
      for (var i = startIndex; i <= stopIndex-1; i++) {
        loadedRowsMap[i] = STATUS_LOADED;
      }
      json.map(user => list.push(user))
    })
}

// Render your list
ReactDOM.render(
  <InfiniteLoader
    isRowLoaded={isRowLoaded}
    loadMoreRows={loadMoreRows}
    rowCount={remoteRowCount}
  >
    {({ onRowsRendered, registerChild }) => (
      <Table
        width={300}
        height={300}
        ref={registerChild}
        onRowsRendered={onRowsRendered}
        headerHeight={20}
        rowHeight={30}
        rowCount={remoteRowCount}
        rowGetter={({ index }) => list[index]}
      >
        <Column
          label='Id'
          dataKey='id'
          width={100}
          cellDataGetter={({ columnData, dataKey, rowData }) => rowData && rowData.id}
        />
        <Column
          label='Name'
          dataKey='name'
          width={100}
          cellDataGetter={({ columnData, dataKey, rowData }) => rowData && rowData.name}
        />
      </Table>

    )}
  </InfiniteLoader>,
  document.getElementById('root')
);

{% endhighlight %}