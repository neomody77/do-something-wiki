## FAQ
### 找不到lunch菜单
以前都是
`
  source build/envsetup.sh
  lucnh XXX
  make
`
lunch之后找不到菜单, 先 build_build_var_cache 然后重新 lunch 就可以了


### Android15 新的命名规则
lunch sdk_phone64_x86_64-trunk_staging-eng


### 写给Windows用户的AOSP构建开发环境配置指南
https://juejin.cn/post/7188078567022919739
https://github.com/5ec1cff/my-notes/blob/master/cuttlefish-on-wsl.md
https://gist.github.com/startergo/4428c78ace77d229357b4a205f38a57a
https://2net.co.uk/blog/cuttlefish-android12.html
```bash
crosvm D 06-07 10:03:32 65542 65542 log_tee.cpp:175] crosvm[1]: libminijail[1]: cannot mount '/usr/lib' as '/var/empty/usr/lib' with flags 0x1001: Invalid argument
crosvm D 06-07 10:03:32 65542 65542 log_tee.cpp:175] crosvm[1]: libminijail[1]: mount_one failed with /dev at '(null)'

## https://stackoverflow.com/questions/78592896/crosvm-gives-a-mounting-error-in-wsl2-when-launching-cuttlefish
## /var/empty/usr/lib 缺少这个文件夹 或者 操作权限 创建并给用户正确授权就正常了

```
