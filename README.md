# Cursor 设备管理工具

这个工具可以帮助您管理 Cursor 编辑器的设备ID和授权信息，支持Windows和macOS系统。

## 功能

1. **重新生成设备ID**: 重置设备ID并清空所有认证信息
2. **读取Token**: 显示当前存储的访问令牌
3. **设置Token**: 设置新的访问令牌并更新设备ID
4. **显示使用情况**: 查看当前账号的使用情况和会员信息
5. **修补机器码获取逻辑**: 修补特定版本的机器码获取方式

## 使用方法

### 图形界面

直接运行程序，将显示交互式菜单：

```
./device-manager
```

### 命令行参数

也可以通过命令行参数直接调用特定功能：

- 重新生成设备ID: `./device-manager regenerate`
- 读取Token: `./device-manager token`
- 设置Token: `./device-manager token set`
- 查看使用情况: `./device-manager usage`
- 修补机器码获取逻辑: `./device-manager patch`

## 编译方法

```bash
# 安装依赖
go mod download

# 编译
go build -o device-manager
```

## 注意事项

1. 本工具会修改Cursor的配置文件，操作前会自动备份，但建议手动备份以防万一
2. 修改设备ID会导致Cursor退出登录状态
3. Windows中可能需要以管理员权限运行才能修改某些文件
4. 修补机器码功能仅适用于特定版本的Cursor

## 系统要求

- Windows 7+ 或 macOS 10.12+
- 已安装Cursor编辑器
