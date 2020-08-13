# rime-symbolic

rime 符號輸入方案

![demo](demo/demo.png)

簡化字版：[sgalal/rime-symbolic-simp](https://github.com/sgalal/rime-symbolic-simp)

## 用法

在 rime 用户資料夾中加入 `symbolic.dict.yaml`。

在常用方案的 `*.schema.yaml` 中加入：

1. `switches` 中加入

```yaml
  - name: symbolic
    reset: 1
    states: [ 無符號, 有符號 ]
```

2. `engine` 的 `filters` 中加入：

```yaml
  - simplifier@symbolic
```

3. 在文件末尾加入：

```yaml
symbolic:
  opencc_config: symbolic.json
  option_name: symbolic
  tips: all
```

在常用方案的 `*.dict.yaml` 中加入：

```yaml
import_tables:
  - symbolic
```

將 `opencc` 資料夾中的文件放入 rime 用户資料夾中的 `opencc` 資料夾中。

重新部署即可。
