# Terminal_Vim_Theme
Theme set up for terminal and vim

## Terminal
### Xterm
在 .bashrc 添加:
```shell
export TERM=xterm-256color
```

### Ubuntu terminal
下载[solarized theme for GNU ls](https://github.com/seebi/dircolors-solarized)
```shell
git clone git://github.com/seebi/dircolors-solarized.git
```
dircolor-solarized: 选择深色系 dark256：
```shell
cp ~/dircolors-solarized/dircolors.256dark ~/.dircolors
```

接下来下载 Solarized 的 Gnome-Terminal 配色：
```shell
git clone git://github.com/sigurdga/gnome-terminal-colors-solarized.git
```
到该目录下运行配色脚本：

```shell
cd gnome-terminal-colors-solarized
```
可以自由切换深色和浅色。
```shell
./set_dark.sh 或./set_light.sh，
```
或者./solarize 也可切换，比如执行一次是dark，再一次变light。如此交替。
