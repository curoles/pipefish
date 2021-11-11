Install Qt on Ubuntu and quickly check installation
---------------------------------------------------

Follow steps at [](https://wiki.qt.io/Install_Qt_5_on_Ubuntu):

1. `sudo apt-get install qt5-default`
2. download from https://www.qt.io/download-open-source#section-2
3. `chmod +x ~/Downloads/qt-unified-linux-x64-4.1.1-online.run`
4. run the installer, create Qt account

```c++
#include <QtWidgets/QtWidgets>

int main(int argc, char* argv[])
{
    QApplication app(argc, argv);
    QPushButton *button = new QPushButton("Hello world!");
    button->show();
    return app.exec();
}
```

```terminal
$ g++ -fPIC test.cpp -o test -I/usr/include/x86_64-linux-gnu/qt5/ -L/home/ilesik/Qt/Tools/QtCreator/lib/Qt/lib/ -lQt5Widgets -lQt5Core
```
