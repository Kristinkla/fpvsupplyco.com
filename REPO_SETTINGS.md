# 仓库设置与上线操作指南

本指南用于把 `Kristinkla/fpvsupplyco.com` 仓库配置成一个**能被搜索、能带来流量**的官方资料型仓库。

> ⚠️ 操作前请先读这份文件，仓库后台的字段填错了会削弱 SEO 效果。

---

## 一、当前仓库状态（诊断结果）

| 项目 | 当前值 | 状态 |
|---|---|---|
| 仓库名 | `fpvsupplyco.com` | ✅ 域名做仓库名，利于品牌词匹配 |
| Description | `fpvsupplyco.com is a FPV Parts, Wholesale & Custom Drones solution supplier.` | ✅ 已填，可优化 |
| **Homepage** | **空** | ❌ **必须填，这是最重要的外链入口** |
| **Topics** | **空** | ❌ **必须填，影响仓库被发现** |
| **文件内容** | **0 文件 / 0 分支** | ❌ **空仓库无排名，等于白发** |
| Stars / Forks | 0 / 0 | ⚪ 需要时间沉淀 |
| License | 无 | ⚪ 可选 |
| 创建时间 | 2026-09-14 | ⚪ 新仓库，需要时间 |

**核心结论：目前这个仓库在 Google 眼中不存在。必须补内容 + 填 Homepage + 填 Topics 三步走。**

---

## 二、第一步：填写 Homepage 字段（最高优先级）

这是整个仓库**最能带来点击的外链位置**——会显示在仓库页面右上角侧栏，是一个醒目、可点击的官网入口。

**操作路径：**
1. 打开 `https://github.com/Kristinkla/fpvsupplyco.com`
2. 点击页面右侧 **⚙️ Settings**（齿轮图标，不是顶部导航的 Settings）
3. 找到 **Website** 输入框
4. 填入：

```
https://fpvsupplyco.com
```

5. 点击 **Save**

**效果：** 仓库页面侧栏顶部会出现带地球图标的 `fpvsupplyco.com` 链接，所有访问仓库的人都能看到并点击。

---

## 三、第二步：优化 Description 与 Topics

### 3.1 Description（仓库描述）

当前描述可用，但可以更利于搜索。建议替换为：

```
FPV parts supplier for builders, distributors and brands — flight controllers, ESC stacks, motors, frames, cameras. Wholesale & OEM/ODM custom drone solutions. Official resource repo for fpvsupplyco.com
```

**理由：** 覆盖了 `FPV parts`、`flight controllers`、`ESC stacks`、`motors`、`frames`、`wholesale`、`OEM` 等买家实际会搜的词，同时保留了官网域名。

> 位置：仓库主页右侧 **About** 区域 → 齿轮图标 → Description 输入框（限 350 字符）

### 3.2 Topics（话题标签）

Topics 会显示在仓库页面顶部，是 Google 判断仓库主题的重要信号。建议填以下（GitHub 限 20 个）：

```
fpv
fpv-drone
drone
drones
drone-parts
fpv-parts
flight-controller
esc
brushless-motors
carbon-fiber-frame
quadcopter
uav
wholesale
oem
odm
drone-supplier
fpv-components
diy-drone
drone-manufacturer
rc-hobby
```

**操作路径：** 仓库主页右侧 **About** 区域 → 齿轮图标 → **Topics** 输入框 → 逐个输入后按回车。

### 3.3 勾选推荐选项

在同一设置面板中：

- ✅ **Releases** — 如果以后发布产品更新/资料版本
- ✅ **Packages** — 可选
- ⬜ **Deployments** — 不需要
- ✅ **Issues** — **保持开启**（客户可以在这里提问，增加仓库活跃度信号）

---

## 四、第三步：上传文件内容

### 4.1 需要上传的文件清单

```
fpvsupplyco.com/
├── README.md                                ← 仓库首页主文档
├── REPO_SETTINGS.md                         ← 本文件（可上传，也可不上传）
└── docs/
    ├── fpv-component-selection-guide.md     ← FPV 选型指南
    ├── fpv-glossary.md                      ← FPV 术语表
    ├── wholesale-oem-guide.md               ← 批发/OEM 指南
    └── faq.md                               ← 常见问题
```

### 4.2 方式 A：网页端上传（推荐，最快）

**上传 README.md：**

1. 打开 `https://github.com/Kristinkla/fpvsupplyco.com`
2. 页面中间会显示 **"Quick setup — if you've done this kind of thing before"**，点击下方的 **`creating a new file`** 链接（或访问 `https://github.com/Kristinkla/fpvsupplyco.com/new/main`）
3. 文件名填：`README.md`
4. 把本地产出的 `README.md` 内容**完整粘贴**进去
5. 底部 Commit message 填：`Add repository README with official website links and product overview`
6. 点击 **Commit new file**

**上传 docs 文件夹：**

1. 回到仓库主页，点击 **Add file** → **Upload files**
2. 在文件名输入框里输入 `docs/` 然后回车（GitHub 会自动创建文件夹）
   - 或直接把整个 `docs` 文件夹从本地拖拽到上传区域，GitHub 会保留目录结构
3. 拖入 `docs/` 下的 4 个 md 文件
4. Commit message 填：`Add FPV reference documentation — selection guide, glossary, wholesale guide, FAQ`
5. 点击 **Commit changes**

### 4.3 方式 B：命令行上传

如果你本地装了 Git：

```bash
# 1. 克隆空仓库
git clone https://github.com/Kristinkla/fpvsupplyco.com.git
cd fpvsupplyco.com

# 2. 复制产出的文件进来（README.md 和 docs/ 文件夹）

# 3. 提交并推送
git add .
git commit -m "Add README and FPV reference documentation"
git branch -M main
git push -u origin main
```

> 如果推送时要求认证，GitHub 已不支持密码登录，需要创建 Personal Access Token 当密码用，或配置 SSH key。

---

## 五、第四步：可选增强项

### 5.1 添加 LICENSE

如果这份文档允许他人自由使用，加个 License 能提升仓库可信度：

1. 仓库主页 → **Add file** → **Create new file**
2. 文件名填 `LICENSE`
3. 点击右上角 **Choose a license template** → 选 **MIT License** 或 **Creative Commons Attribution 4.0**（文档类推荐 CC BY 4.0）
4. Commit

### 5.2 添加产品目录 CSV（可选，对 SEO 帮助大）

把官网产品导出成 CSV 放进仓库，比如 `data/product-catalog.csv`。这样仓库就有了**可被搜索的具体产品数据**，而不仅是介绍文字。表格如果能被 Google 收录为结构化内容，价值更高。

### 5.3 定期更新

- 保持 **每月至少一次提交**（更新产品、补充文档）
- 提交历史会显示在仓库首页，活跃的仓库在 Google 眼中更可信
- 不要一次性堆几百个文件然后放着不管——那反而像垃圾仓库

---

## 六、重要提醒：关于外链效果的预期管理

### 6.1 README 链接是 nofollow

GitHub 页面上的正文链接（README 里的 `[链接](url)`）默认带 `rel="nofollow"`，**不会直接把权重传给 fpvsupplyco.com**。

**真正有效的三个位置：**
1. **Homepage 字段** —— 侧栏显著位置，点击率最高
2. **Description 里的域名** —— 被反复抓取
3. **Topics** —— 帮助仓库本身出现在相关搜索里

**所以策略重心应该是：让仓库本身有排名 → 用户点进来 → 通过 Homepage 或正文链接进官网。**

### 6.2 空仓库无价值

Google 对空仓库的处理是**不索引**。这也是为什么"只建仓库不填内容"这个做法完全无效——必须要有真实内容。

### 6.3 不要做成纯 SEO 农场

❌ **会被判定为 spam 并封号的做法：**
- 建几十个仓库，每个只放一行官网链接
- 仓库名堆砌关键词（如 `fpv-parts-wholesale-drone-supplier-best-price`）
- 用脚本批量刷 star / fork
- 重复内容复制到多个仓库

✅ **可持续的做法：**
- 少量高质量仓库，每个有真实独立的内容
- 仓库名用品牌词（你现在这样 `fpvsupplyco.com` 就是对的）
- 内容对 FPV 用户有实际价值（选型、术语、FAQ 这类天然有价值）
- 自然增长，不刷量

### 6.4 长期价值在于"被搜到"

GitHub 域名的权重极高，仓库页在 Google 上排名通常很好。如果你的仓库内容能覆盖 **"fpv parts supplier"**、**"flight controller stack"**、**"drone wholesale"** 这类词，就能持续带来真实搜索流量——**这比传权重更稳、更持久。**

---

## 七、执行清单

按顺序完成以下事项：

- [ ] **1. 填 Homepage 字段** → `https://fpvsupplyco.com`（最重要）
- [ ] **2. 更新 Description** → 用本文档 3.1 的文案
- [ ] **3. 添加 Topics** → 用本文档 3.2 的 20 个标签
- [ ] **4. 上传 README.md** → 仓库首页主文档
- [ ] **5. 上传 docs/ 文件夹** → 4 个参考资料文件
- [ ] **6. 确认 Issues 已开启** → 让客户能提问
- [ ] **7. （可选）添加 LICENSE** → CC BY 4.0
- [ ] **8. （可选）上传产品 CSV** → data/product-catalog.csv
- [ ] **9. 设置每月更新提醒** → 保持仓库活跃

---

## 八、验证效果

完成上传后，用以下方式验证：

1. **直接访问** `https://github.com/Kristinkla/fpvsupplyco.com` —— README 应该正常渲染，链接可点击
2. **检查 Homepage** —— 侧栏应显示 `fpvsupplyco.com` 链接
3. **Google 搜索** `site:github.com Kristinkla fpvsupplyco` —— 几周后应能被收录
4. **Google Search Console** —— 如果 fpvsupplyco.com 已接入 GSC，可以在"链接"报告里观察来自 github.com 的引用

> 收录需要时间，通常 1–4 周。新仓库不要期待立刻见效。
