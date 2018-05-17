Mac终端操作命令

1.Mac命令行里的复制，粘贴与合并
a.copy到剪切板
cat a.txt | pbcopy
---
b.paste大文本
比如从excel中copy一个百万行记录后，需要粘贴到文本中，可以在终端执行: pbpaste > tmp.txt
---
c.替换^M
从excel中copy出来，然后通过pbpaste粘贴后，文本里的换行可能会成为^M，所有数据在一行显示：这时可通过vim运行"%s/^M/\r/g"
^M=Ctrl+v Ctrl+m
---
d.合并
按行合并: pbpaste t1 t2