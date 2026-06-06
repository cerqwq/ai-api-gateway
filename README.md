# 🚪 AI API Gateway

AI API网关工具，支持网关设计、路由、限流。

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python" />
  <img src="https://img.shields.io/badge/OpenAI-API-green?logo=openai" />
  <img src="https://img.shields.io/badge/License-MIT-yellow" />
</p>

## ✨ 特性

- 🏗️ API网关设计
- ⚙️ Nginx配置生成
- ⚡ 限流器生成
- 🔄 API版本管理
- 🛡️ 熔断器生成
- 📖 API文档生成

## 🚀 快速开始

```bash
pip install openai

python tools.py
```

## 📖 使用

```python
from ai_api_gateway import create_tools

tools = create_tools()

# API网关设计
gateway = tools.design_api_gateway(["用户服务", "订单服务"], "高可用")

# Nginx配置
nginx = tools.generate_nginx_config(services)

# 限流器
limiter = tools.generate_rate_limiter("令牌桶", {"rpm": 1000})

# API版本管理
versioning = tools.design_api_versioning("v1", ["新功能"])

# 熔断器
breaker = tools.generate_circuit_breaker("支付服务", thresholds)

# API文档
docs = tools.generate_api_docs(endpoints)
```

## 📁 项目结构

```
ai-api-gateway/
├── tools.py       # API网关工具核心
└── README.md
```

## 📄 许可证

MIT License
