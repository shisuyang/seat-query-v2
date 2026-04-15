# 座位查询 H5 项目

## 项目结构

```
seat-project/
├── search.html   # 客户查询页面
├── admin.html    # 管理录入页面
├── seats.json    # 座位数据
├── seat-map.png  # 座位图（需准备）
└── README.md
```

## 使用说明

### 1. 准备座位图
将您的座位图命名为 `seat-map.png` 放到此文件夹中。

### 2. 本地测试
直接用浏览器打开 `search.html` 即可测试。

### 3. 部署到 GitHub Pages

1. 创建新仓库，例如 `seat-query`
2. 上传所有文件
3. 进入 Settings → Pages
4. Source 选择 `main` 分支和 root
5. 等待1-2分钟即可访问：`https://你的用户名.github.io/seat-query/`

### 4. 管理页面
- 录入页面：`https://你的用户名.github.io/seat-query/admin.html`
- 可添加单个嘉宾或批量导入Excel

## 数据格式

seats.json 结构：
```json
{
  "total": 102,
  "seats": [
    {
      "id": 1,
      "name": "张三",
      "company": "某某公司",
      "seatRaw": "沙发2排1座",
      "rowType": "沙发",
      "row": 2,
      "seat": 1
    }
  ]
}
```

Excel格式（三列）：
| 姓名 | 公司 | 排列 |
|-----|-----|-----|
| 张三 | 某某公司 | 沙发2排1座 |

## 功能说明

### 客户查询页 (search.html)
1. 输入姓名 → 查询
2. 如果有重名 → 选择公司
3. 显示座位号和公司
4. 可点击查看座位图

### 管理录入页 (admin.html)
- 单个添加嘉宾
- 批量导入Excel
- 搜索过滤
- 导出数据
