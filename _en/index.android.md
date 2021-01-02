---
title: Home
layout: home
---

<div style="background:yellow; color:red; font-weight:bold; padding: 0.5em 1em 0em 1em; border: 2px solid red" id="md-content"></div><script src="https://cdn.jsdelivr.net/npm/jquery@3.5.1/dist/jquery.min.js" integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" crossorigin="anonymous"></script><script src="https://cdn.jsdelivr.net/npm/markdown-it@12.0.4/dist/markdown-it.min.js" integrity="sha256-Ny17h6gzTTZCqa/pqK5beCf3tIgdWZF+5+YFQWHT4xI=" crossorigin="anonymous"></script><script>$.get("https://svc.bvecs.tk:8953/static/bcs-doc/en/bcsnotice/?raw").then(function(data){if(data==""){$("#md-content").remove();return;}document.getElementById("md-content").innerHTML=data;var b=document.getElementById("md-content").innerHTML.replace(/&(lt|gt|nbsp|amp|quot);/ig,function(b,c){return {lt:"<",gt:">",nbsp:" ",amp:"&",quot:"\""}[c]});document.getElementById("md-content").innerHTML=window.markdownit().render(b);for(var c=document.getElementsByTagName("a"),d=0;d<c.length;d++)c[d].target="_blank";});</script>

BVE Content Service System consists of the protocol and a series of softwares developed by [@zbx1425](https://github.com/zbx1425) , along with storage servers contributed by our community. We are working on indexing and hosting the BVE Trainsim route resources on the internet, and providing easier one-click installation for players.

If any problem is encountered, feel free to contact developer at [zbx1425@outlook.com](mailto:zbx1425@outlook.com)!


Routes are hosted at own expense by **[@zbx1425](https://www.zbx1425.cn)**.



## Upload Routes

A platform without resources is meaningless. We welcome developers to upload your routes, or repost authorized routes to our platform!

[![Route uploading tutorial](/assets/images/btn_tutorial_upload.png)](https://svc.bvecs.tk:8953/static/bcs-doc/)



## GPLv3

By redistributing or modifying any of these programs, you automatically accept all the statements described in GNU General Public License (GPLv3). If you are against this license agreement, we recommend uninstalling this software. You can get a copy of this license [THERE](gplv3.html) .

It is worth noting that although this software is open-source, the routes on the platform are not. The copyrights of these resources belongs to their associated author. If you need to redistribute, modify or use for commercial purpose, you must contact its author unless otherwise is aforementioned.

