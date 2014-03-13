# install git
# sudo aptitude install git
# git clone https://github.com/mzgcz/self-rex.git
# git clone https://github.com/mzgcz/self-repository.wiki.git

# install rex
# sudo aptitude install libnet-ssh2-perl curl openssh-server
# curl -L get.rexify.org | perl - --sudo -n Rex

group myserver => "127.0.0.1";

desc "软件包说明";
task "readme", group => "myserver", sub {
  say "康柏自由人笔记本驱动：intel-microcode, firmware-b43-installer";
  say "goagent代理网址：https://code.google.com/p/goagent/";
  say "flashplugin-nonfree：该软件特殊，需要root在命令行设置代理后进行安装";
  say "字体infinality设置参考网址：http://blog.csdn.net/renhuailin/article/details/18037405"
};

desc "安装系统软件包";
task "prepare", group => "myserver", sub {
  install [qw/sawfish/];
  install [qw/nitrogen/];       # 壁纸设置工具
  install [qw/vim/];
  install [qw/fcitx im-switch fcitx-googlepinyin/]; # 输入法
  install [qw/emacs24 cscope-el libnotify-bin yasnippet clang/];
  install [qw/ttf-bitstream-vera ttf-wqy-microhei ttf-wqy-zenhei/]; # 字体
  install [qw/sbcl racket/];                                        # lisp相关
  install [qw/yakuake/];                                            # 终端
  install [qw/build-essential/];                                    # 编译工具
  install [qw/python-openssl libnss3-tools python-crypto/];         # goagent代理
  install [qw/axel/];                                               # 下载工具
  install [qw/unrar/];
};

desc "设置用户链接";
task "usr_link", group => "myserver", sub {
  run "ln -s ~/self-repository.wiki/emacs/configure/.emacs.d ~/.emacs.d";
  run "ln -s ~/self-repository.wiki/system/sawfish/.sawfish ~/.sawfish";
};

desc "设置系统链接";
task "sys_link", group => "myserver", sub {
  run "ln -s ~/self-repository.wiki/system/sawfish/RedMILL /usr/share/sawfish/themes/RedMILL";
};
