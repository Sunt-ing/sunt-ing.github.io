### Shell配置文件

- **交互式 shell**：**在终端有交互的模式，用户输入命令，并在回车后立即执行的 shell**，这种模式也是大部分情况下用户执行的一种方式，比如 ssh 登录
- **非交互式 shell**：**bash shell 以命令脚本的形式执行**，shell 不会和用户有交互，而是读取脚本文件并执行，直到读取到文件 EOF 时结束
- **login shell**：
  - 举例
    - 通过用户名和密码登入，如 ssh 
    - 通过带 --login 参数的命令：bash --login 而启动的 shell
  - 读取的配置文件
    - bash：`/etc/profile` > `~/.bash_profile`  > `~/.bash_login` > `~/.profile` \> `.bash_logout`
      - 如果 `~/.bash_profile` 或 `~/.bash_login` 存在就不会读取 `~/.profile`
    - zsh：`/etc/zprofile` 和 `~/.zprofile`
- **non-login bash**：登录以后所打开的 bash
  - 举例
    - 通过 Ctrl+Alt+T 组合键打开的 bash 环境，直接通过 bash 命令打开的环境
    - 你在已经存在的终端 session 中开启一个 shell
    - shell 执行一个脚本，这种 shell 无处不在，在程序调用另外一个程序时非常常见
  - 读取的文件
    - bash：`~ /.bashrc` 
    - zsh：`/etc/zshrc` 和 `~/.zshrc`



### 实际例子

**VS Code**：在VS Code上远程连接Linux环境后开启terminal时，使用的是非登入shell，所以只会 source ``~.bashrc`

**WSL**：是登入shell，不source ~/.bashrc，但是会 source ~/.bash_profile



### 参考

- [登录式 shell 和非登录式 shell 区别](http://einverne.github.io/post/2019/01/login-shell-vs-non-login-shell.html)
- [remote-ssh: .profile not sourced for bash shells, only .bashrc?](https://github.com/microsoft/vscode-remote-release/issues/83)



