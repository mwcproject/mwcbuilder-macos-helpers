Here are all tools needed to build

QT 5.9 are cleaned from non needed libs and plugins

ls -al  QT/5.9/clang_64/lib/
total 102504
drwxr-xr-x  119 kbay  staff      3808 Nov 29 13:51 .
drwxr-xr-x    8 kbay  staff       256 Nov 29 13:05 ..
-rw-r--r--@   1 kbay  staff      6148 Nov 29 13:53 .DS_Store
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtCore.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtCore.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtGui.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtGui.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtMacExtras.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtMacExtras.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtNetwork.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtNetwork.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtPrintSupport.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtPrintSupport.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtSvg.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtSvg.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtTest.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtTest.framework.dSYM
drwxr-xr-x    9 kbay  staff       288 May 21  2019 QtWidgets.framework
drwxr-xr-x    3 kbay  staff        96 May 21  2019 QtWidgets.framework.dSYM
drwxr-xr-x   15 kbay  staff       480 Nov 29 13:03 cmake


ls -al  QT/5.9/clang_64/plugins/
total 16
drwxr-xr-x   5 kbay  staff   160 Nov 29 13:53 .
drwxr-xr-x   8 kbay  staff   256 Nov 29 13:05 ..
-rw-r--r--@  1 kbay  staff  6148 Nov 29 13:53 .DS_Store
drwxr-xr-x  14 kbay  staff   448 May 21  2019 platforms
drwxr-xr-x   6 kbay  staff   192 May 21  2019 printsupport


How to compress:
tar cvfj qt_59.tar.bz2 QT/5.9
split -b 60m -a 3 qt_59.tar.bz2 qt_59_

Results: qt_59_aaa  & qt_59_aab


How to extract:

cat qt_59_aaa qt_59_aab | bzip2 -dc | tar xvf -
