# Spring AI 框架介绍

## 🎯 是什么
Spring AI是Spring官方推出的AI应用开发框架，基于Spring生态构建，为Java开发者提供简洁、统一的AI应用开发体验。它将AI能力无缝集成到Spring应用中，让开发者能够轻松构建智能化的企业级应用。

## 🔧 解决的问题
- **Spring生态集成**：与Spring Boot、Spring Cloud等无缝集成
- **AI模型复杂性**：抽象AI模型差异，提供统一接口
- **企业级需求**：满足企业应用的安全性、可观测性要求
- **开发效率低**：简化AI应用开发，提升开发效率
- **运维复杂**：提供Spring生态的运维和监控能力

## 🚀 核心模块

### **1. AI模型抽象 (Model Abstraction)**
- **统一接口**：ChatClient、EmbeddingClient等统一接口
- **多模型支持**：OpenAI、Azure OpenAI、Anthropic等
- **本地模型**：支持Ollama、本地部署模型
- **模型配置**：通过Spring配置管理模型参数

### **2. 提示工程 (Prompt Engineering)**
- **提示模板**：支持Thymeleaf、FreeMarker等模板引擎
- **动态提示**：支持变量替换和条件逻辑
- **提示管理**：集中管理提示词模板
- **多语言支持**：国际化提示词支持

### **3. 向量存储 (Vector Store)**
- **文档处理**：支持多种格式文档加载和分块
- **向量化**：文本向量化和存储
- **相似性搜索**：基于向量的语义搜索
- **RAG应用**：检索增强生成应用支持

### **4. 函数调用 (Function Calling)**
- **工具集成**：丰富的内置工具库
- **自定义函数**：支持开发者自定义函数
- **函数注册**：通过Spring Bean注册函数
- **参数验证**：Spring Validation集成

### **5. 流式处理 (Streaming)**
- **流式响应**：支持AI模型的流式输出
- **响应式编程**：与Spring WebFlux集成
- **实时交互**：支持实时对话和交互
- **性能优化**：提升用户体验和系统性能

### **6. 安全与监控 (Security & Monitoring)**
- **Spring Security**：与Spring Security集成
- **可观测性**：Micrometer、Actuator集成
- **审计日志**：AI操作审计和日志记录
- **性能监控**：AI调用性能监控和分析

## 💻 快速开始

### **Maven依赖**
```xml
<dependency>
    <groupId>org.springframework.ai</groupId>
    <artifactId>spring-ai-openai-spring-boot-starter</artifactId>
    <version>0.8.0</version>
</dependency>
```

### **基础使用示例**
```java
@Service
public class AiService {
    
    @Autowired
    private ChatClient chatClient;
    
    public String chat(String message) {
        return chatClient.call(message);
    }
}
```

### **配置文件**
```yaml
spring:
  ai:
    openai:
      api-key: ${OPENAI_API_KEY}
      base-url: ${OPENAI_BASE_URL}
```

## 🌟 特色功能
- **Spring原生**：完全基于Spring生态构建
- **自动配置**：Spring Boot自动配置支持
- **企业级特性**：安全性、可观测性、监控等
- **云原生**：支持云原生部署和扩展
- **测试支持**：Spring Test集成，测试友好

## 🔗 相关链接
- **GitHub**: https://github.com/spring-projects/spring-ai
- **官网**: https://spring.io/projects/spring-ai
- **文档**: https://docs.spring.io/spring-ai/reference/
- **示例**: https://github.com/spring-projects/spring-ai-samples

## 📝 总结
Spring AI为Java开发者提供了与Spring生态深度集成的AI开发框架，通过统一接口、自动配置和企业级特性，让开发者能够快速构建安全、可观测的AI应用。其Spring原生设计使其成为Spring开发者构建AI应用的最佳选择。
