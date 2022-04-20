# README

Firstly download the *stackoverflow-posts.7z* from the magnet link given below. The stackoverflow.com-Posts.7z file contains the dump for the Posts table (that is, questions and answers). The size of the folder is 17GB which go upto 68GB after unzipping.

**Link :**

```
magnet:?xt=urn:btih:2CADCY4DQZUPORG55KW5GUL6RWZ3FN6Z&dn=stackoverflow.com-Posts.7z&tr=http%3A%2F%2Fbt1.archive.org%3A6969%2Fannounce
```

Run the following commands after finish the downloads.

```
python download.py
```

We need to parse the xml file into json and map answer to question. Since the initial file is too big to use single thread, use map-reduce framework for multithread to parse efficiently. We have to split the big input file into several small files first.

```
python parse_post.py
```

Finally, we need to extract the urls.

```
python extract_post.py
```
