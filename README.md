# 🐾 宠物领养小程序 - 更多在微信 ： jackSinWu --在咸鱼：不知名选手java小鑫 --B站：不知名选手java小鑫 关注可打9折

**宠物领养小程序** 是一个集成了宠物送养、领养申请、寻宠启事、用户打卡签到、积分兑换商城等功能于一体的综合性公益平台。旨在为流浪宠物寻找温暖的家，同时鼓励用户通过打卡和互动积攒积分，兑换宠物相关物品，形成良性生态。
![image](https://github.com/user-attachments/assets/e365cc34-b5bc-4d28-a20e-f5835cff63f8)

![image](https://github.com/user-attachments/assets/8b524e57-032a-45f9-bff2-a32440b2578a)

![image](https://github.com/user-attachments/assets/c430089f-31b3-42dd-98b9-d87db4c44ed4)

![image](https://github.com/user-attachments/assets/b3d357cc-0cd9-4e75-ab55-f16c825281b6)

![image](https://github.com/user-attachments/assets/a75730bd-44ca-4db8-8a3b-cc61bc052deb)

![image](https://github.com/user-attachments/assets/4e91efd1-b5d8-48b4-9105-f002780fcbb3)

![image](https://github.com/user-attachments/assets/c31a064d-3507-4c96-98d7-89b6924ef2df)

![image](https://github.com/user-attachments/assets/03729d41-49b9-4e31-b0d3-ea88ed938992)

![image](https://github.com/user-attachments/assets/695d8ef9-da60-465d-a54d-203ee84ce5c5)

![image](https://github.com/user-attachments/assets/b85f1b9f-f5b8-4a0a-9c08-fcfe3495ba83)

![image](https://github.com/user-attachments/assets/87c0bec2-0faf-4fde-9a47-ff8fcc114b2d)

![image](https://github.com/user-attachments/assets/2be1ba65-79c2-4341-ad77-3653ca73f27f)

---

## 🛠 技术栈

- **前端**：Vue.js + Vuex + UniApp
- **后端**：Spring Boot + MyBatis + Shiro + WebSocket  
- **数据库**：MySQL  
- **文件存储**：MinIO（用于图片、视频上传）  

---

## 🌟 核心功能模块

### 1. 用户管理模块

- 用户注册与登录（微信授权或手机号注册）  
- 实名认证（提高领养人与送养人信用）  
- 个人信息管理（头像、昵称、领养记录、送养记录）  
- 消息通知系统（领养通知、评论消息、系统公告）

---

### 2. 宠物送养模块

- 发布送养信息（填写宠物信息、上传照片）  
- 宠物信息包括：种类、年龄、性别、健康状况、疫苗情况、送养理由等  
- 审核机制：后台管理员审核后发布  
- 查看送养申请列表，选择领养人进行沟通  
- 管理送养状态（待领养 / 已领养 / 撤销送养）

---

### 3. 宠物领养模块

- 浏览可领养宠物列表（支持筛选：类别、年龄、性别等）  
- 提交领养申请（填写领养条件、联系方式）  
- 查看申请状态、历史申请记录  
- 签署电子领养协议（支持 PDF 下载）  
- 积分奖励：成功领养后奖励积分

---

### 4. 寻宠启事模块

- 发布寻宠信息（丢失地点、时间、宠物特征、照片）  
- 浏览丢失启事、提供线索  
- 联系发布人、评论留言互动  
- 状态管理：寻找中 / 已找回  
- 公告推送：附近用户收到提醒

---

### 5. 打卡签到模块

- 每日打卡签到（积分奖励）  
- 连续签到奖励制度  
- 查看签到记录与积分变动明细  
- 打卡日历可视化（展示用户活跃度）

---

### 6. 积分商城模块

- 通过打卡、领养、送养等行为获取积分  
- 浏览兑换商品（宠物用品、周边商品、服务券等）  
- 商品分类与库存管理  
- 创建兑换订单，积分抵扣下单  
- 兑换记录管理（订单状态、发货信息）

---

### 7. 后台管理模块（管理员端）

- 用户管理（实名认证审核、违规封号）  
- 宠物信息审核（送养 / 寻宠）  
- 商品与订单管理（上下架、库存、发货）  
- 内容管理（评论审核、举报处理）  
- 系统配置（积分规则、公告发布）  
- 数据统计（领养成功率、活跃用户、积分发放）

---

## 🚀 项目部署指南

### ✅ 环境要求

| 环境组件 | 版本要求 |
|----------|----------|
| JDK      | 11+ |
| Node.js  | 16+ |
| MySQL    | 8+ |
| MinIO    | 任意稳定版本 |

---

### ▶ 后端启动步骤

```bash
# 进入后端项目目录
cd backend

# 构建后端项目
mvn clean package

# 启动 Spring Boot 应用
java -jar target/pet-adoption-system.jar
```

---

### ▶ 前端启动步骤

```bash
# 进入前端项目目录
cd frontend

# 安装依赖
npm install

# 启动项目
npm run serve
```

> 若使用 UniApp 构建微信/支付宝小程序版本，可使用 HBuilderX 或 cli 构建发布。

---

### ▶ MinIO 配置说明

```bash
# 启动 MinIO 示例
minio server /data --console-address ":9001"
```

- 控制台地址：[http://localhost:9001](http://localhost:9001)
- 在 `application.yml` 配置：

```yaml
minio:
  endpoint: http://localhost:9000
  accessKey: your-access-key
  secretKey: your-secret-key
  bucketName: pet-assets
```

---

## 📁 项目目录结构

```
pet-adoption-app/
├── backend/          # Spring Boot 后端
│   ├── src/main/
│   ├── resources/
│   └── pom.xml
├── frontend/         # Vue 或 UniApp 小程序前端
│   ├── src/
│   ├── public/
│   └── package.json
├── docs/             # 项目说明文档
├── README.md         # 项目说明
```

---

## 🧠 项目亮点

- 🐶 贴合真实领养流程，兼顾送养人和领养人需求  
- 📍 支持寻宠地图发布，提升找回成功率  
- 🎁 积分体系激励活跃，提升平台粘性  
- 🔐 完善的审核与后台管理机制保障平台内容安全  
- 🧩 可拓展为公益宠物救助平台或社区宠物交流平台

---

## 📌 注意事项

- 图片/视频建议使用 CDN 或对象存储加速加载  
- 微信小程序需配置对应小程序 AppID 和域名白名单  
- 本项目为学习 / 教学示范项目，可根据实际业务拓展功能

