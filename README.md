[![Build status](https://ci.appveyor.com/api/projects/status/r40jjjseyqb0y15h?svg=true)](https://ci.appveyor.com/project/bartoszek/openboard-thirdparty)
OpenBoard third party libraries
================================

These are various libraries that OpenBoard depends on and that may not be included with your OS. These should be built before OpenBoard.

Building freetype, quazip and xpdf should be all that is needed. Instructions are provided in each subfolder. For example, to build all libraries on Linux:

## Linux

### Build freetype

    cd freetype
    qmake freetype.pro -spec linux-g++
    make
    cd ..

### Build quazip

    cd quazip
    qmake quazip.pro -spec linux-g++
    make
    cd ..

### Build xpdf

    cd xpdf/xpdf-3.04
    ./configure --with-freetype2-library="../../freetype/lib/linux" --with-freetype2-includes="../../freetype/freetype-2.6.1/include"
    cd ..
    qmake xpdf.pro -spec linux-g++
    make
    cd ..
