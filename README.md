# AWD
### AWD线下攻防常用自动化脚本

已经在平台测试过了，全部可用，适用鲁棒性有待检查。

有任何问题请联系QQ：2903735704

#### Vision 1.0.0

各个文件详解：

#### Python：

protect.py:

功能：

搜索当前目录下文件名包含php的文件（实际上应该搜索包含.php的文件）

统计文件个数，输出

读入一个参数 1 或 0

1 执行对全部统计文件的内容更改，在文件尾加<?php require_once('log.php')?>

0 退出程序


trojan.py

功能：

读入一句话木马名字，例如：123.php

读入要植入的不死马名字，例如 456.php （要和程序内的edit部分一致）

读入要植入的自动读取flag名字，例如 789.php （要和程序内的edit部分一致）

读入要批量上传的队伍数量（请和trojan.txt中的行数一致）

直接循环从trojan.txt读取url（url为上传文件的地址，以/结尾）

通过一句话木马批量植入不死马和自动读取flag

确认成功后每30秒连接一次，确认存活，如果没有存活重复植入


get_score.py

功能：
