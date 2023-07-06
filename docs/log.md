
2023-06-19

在MySQL的docker containter 里，竟然无法连接网络。

查看：

    $ l /etc/resolv.conf
    lrwxrwxrwx 1 root root 29 May 22  2020 /etc/resolv.conf -> ../run/resolvconf/resolv.conf

修改：

    sudo ln -sf /run/systemd/resolve/resolv.conf /etc/resolv.conf

再次查看：

    $ l /etc/resolv.conf
    lrwxrwxrwx 1 root root 32 Jun 19 09:25 /etc/resolv.conf -> /run/systemd/resolve/resolv.conf


