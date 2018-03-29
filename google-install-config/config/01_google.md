<!SLIDE >
# for centos7 with root

在centos7中用root用户打开google，做如下修改：
vi /opt/google/chrome/google-chrome
修改最后一行：
original command:
exec -a "$0" "$HERE/chrome" "$@"
new command:
exec -a "$0" "$HERE/chrome" "$@" --no-sandbox --user-data-dir $HOME
