---
title: My Bash Notepad
author: Duk Lee
authorURL: http://twitter.com/mrduklee
---

```bash
cat b.txt | sed '/plural of/d' | sed '/variant of/d' | sed '/present participle/d' | sed '/present tense third person/d' | sed '/variant spelling/d' | sed '/superlative of/d' | sed '/past tense of/d' | sed -e 's/:&nbsp; //g' > b1.txt

# i before e except after c or when sounded as a as in neighbor or weigh
cat word_only.txt | grep '[abdefghijklmnopqrstuvwxyz]ei' | wc -l
cat word_only.txt | grep '[^c]ei' | wc -l

# list words end with k but not ck
cat word_only.txt | grep '[^c]k$'

# find words that contains more then one 'ə' 
cat pro_only.txt | grep '.*|[^,]*ə[^,]*ə,' | wc -l

# finds words that contains certain chraters. e.g. dd
grep '^[a-z]*dd[a-z]*|' words.txt
```