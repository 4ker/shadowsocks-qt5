Shadowsocks-Qt5
===============

装了 Anaconda，可能你的 qmake 就不是 qt5 的了，会出错。

```bash
$ qmake -v
QMake version 3.0
Using Qt version 5.7.1 in /opt/Qt5.7.1/5.7/gcc_64/lib
```

看你的 qmake 是否正确。我用的官方的 run 文件安装了 qt5，需要自己加一下 PATH。

[![Build Status](https://travis-ci.org/shadowsocks/shadowsocks-qt5.svg?branch=master)](https://travis-ci.org/shadowsocks/shadowsocks-qt5)

Please check [project's wiki](https://github.com/shadowsocks/shadowsocks-qt5/wiki) for "how-tos".

Introduction
------------

Shadowsocks-Qt5 is a native and cross-platform [shadowsocks](http://shadowsocks.org) GUI client with advanced features.

Features
--------

- Shadowsocks-Qt5 is written in C++ with Qt 5.
- Support traffic statistics
- Support server latency (lag) test
- Use multiple profiles simultaneously
- `config.ini` is located under `~/.config/shadowsocks-qt5/` on \*nix platforms, or under the application's directory on Windows.

Note
----

If `ss-qt5` crashes and the **only one instance** mode is checked,
you may need to manually delete `/tmp/qipc_sharedmemory_ShadowsocksQt*`
and `/tmp/qipc_systemsem_ShadowsocksQt*`.
Otherwise, `ss-qt5` will complain that another instance is already running.
Run `ss-qt5` again is also expected to work.

LICENSE
-------

![](http://www.gnu.org/graphics/lgplv3-147x51.png)

Copyright © 2014-2016 Symeon Huang

This project is licensed under version 3 of the GNU Lesser General Public License.
