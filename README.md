主要需求：
路径下已经存在A用户0-9的音频，文件名为1.MP3 2.MP3 ...，发随机的语音验证码过来以后，自动合成语音

前提：
首先需要身份验证，根据前端js传来的idcard判断数据库是否存在该用户
存在，则返回idcard+name的路径（该路径下保存有该用户0-9的音频文件），同时该文件夹下有一个名为new的文件夹，用于保存生成的音频文件
在保存之前，清空new文件，来减小内存的消耗

小记：
因为是内部使用，所以安全策略就过滤了单引号，而且用了强制转换，应该就没啥问题了，至于传了idcard没传code的话，该情况不考虑。
