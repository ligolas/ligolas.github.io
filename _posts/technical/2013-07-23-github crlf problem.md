---
layout:	post
category: technical
title: git CRLF问题手记
description: 记录问题调git时遇到的CRLF问题，主要是用来测试博客的发布问题
---


#{{ page.title }}
1. 直接使用 git check -- filter.js 命令完成，无任何回显，使用git status 查看，filter.js依然处于"changes not staged for commited"
2. 误操作（双击了文件）使得IE弹出了该文件的下载提示框被忽略，结果一直提示文件占用，以为是git或者mingw问题，差点掉沟里
3. 使用git diff 查看不同，得到最后有提示:可能是crlf的问题
4. 修改crlf设置：git config core.autocrlf=true 之后依然有问题
5. 反复修改autocrlf设置和.gtiattributes文件中的设置，问题依然
6. 参照github的关于文件设置的建议的最后一步 https://help.github.com/articles/dealing-with-line-endings 做了重置
7. 情况回复正常，但是没法复现该问题，最后一步操作的理由是 设置之后会尝试re-normalize 所有文件，那么我再修改这些设置的话，文件应该还会尝试re-normalize但是没有发现次情况
8. 感觉真正起了作用的就是重置操作，可以肯定是crlf的问题，但是在尝试复现这个问题的时候，貌似单独哪项都没有起效果，真是怪了
	
	
	