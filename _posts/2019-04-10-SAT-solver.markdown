---
layout:     post
title:      "C++ study note"
subtitle:   " \"A simple implementation of SAT-solver\""
date:       2019-04-10 12:00:00
author:     "Wei"
header-img: "img/post-20190410.png"
catalog: true
tags:
    - 编程
    - C++


---

> "stay hungry, stay foolish"

# Main idea:

brute force

- `regex_search` extract all occurred variables

- `set` delete repeat variables

- `bitset` assign bit values in canonical order to all variables

- `map` to store corresponding values

- `regex_search` find and replace every  internal tuple "\|xy" by "0" or "1", loop until s == "1" or "0"

- `regex_match` handle invalid input

  

# Notes:

- In `regex ` `\\w` represents one letter rather than `\w`. Remmber double slash, same to other special symbols.

- `regex_match` matches whole string with regular expression, but `regex_search` only returns first matched string, if we need to find all, it's not simple like `re.findall` in `python`, rather `while` with arguments `start` and `end` iterator loops.

- Iterator plays an important role in `C++` . Not like `python`, we could `for … in` to go through in different data structures like `set`, `map` and so on. In `C++` the only way to go through a set is `std::map<char, int>iterator iter` then loop it from `map.begin()` to `map.end()`. `iter->first` refers to key, `iter->second` refers to value. Each iterator refers to one bit of original map or string, so that we could execute some bit operations on them.

  link: [SAT-solver](https://github.com/desAweis/programming-challenge/tree/master/SAT-solver)



