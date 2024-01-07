# merge_srt_files

Merge 2 srt files into 1 srt，for making bilingual subtitle file，by the closest timestamp, e.g.

0x1,srt1 is：

.....

1
00:01:01,774 --> 00:01:04,193
<i>Why are the English still with us?</i>

2
00:01:05,236 --> 00:01:07,029
<i>Why, after everything we've thrown at them,</i>

3
00:01:07,113 --> 00:01:09,865
<i>does the British presence in Ireland still endure?</i>

4
00:01:09,949 --> 00:01:13,410
<i>So many sacrifices have been made.</i>

......

0x2,srt2 is：

......

2
00:01:01,774 --> 00:01:03,859
‎英国人为什么还在我们这里？

3
00:01:05,236 --> 00:01:07,780
‎在我们以各种方式 ‎表达了我们对他们的厌恶之后

4
00:01:07,863 --> 00:01:09,865
‎英国人为什么还在爱尔兰持续出现？

5
00:01:09,949 --> 00:01:11,075
‎（死亡女王）

6
00:01:11,158 --> 00:01:13,410
‎人们做了那么多牺牲

7
00:01:14,370 --> 00:01:16,080
‎我们那么多的兄弟姐妹

......

0x3,After merge, you'll get a srt like:

......

2
00:01:01,774 --> 00:01:04,193
<i>Why are the English still with us?</i>
‎英国人为什么还在我们这里？

3
00:01:05,236 --> 00:01:07,029
<i>Why, after everything we've thrown at them,</i>
‎在我们以各种方式 ‎表达了我们对他们的厌恶之后

4
00:01:07,113 --> 00:01:09,865
<i>does the British presence in Ireland still endure?</i>
‎英国人为什么还在爱尔兰持续出现？

5
00:01:09,949 --> 00:01:13,410
{\an8}‎（死亡女王）

6
00:01:09,949 --> 00:01:13,410
<i>So many sacrifices have been made.</i>
‎人们做了那么多牺牲

......


# howto

"Usage: python merge.py basefile_path.srt transfile_path.srt";

"Merged srt will be found next to the basefile_path.srt";
