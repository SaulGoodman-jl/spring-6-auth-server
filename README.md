# Spring Auth Server 项目

## 项目简介
该项目是一个基于Spring Security和Spring Authorization Server的OAuth2授权服务器，支持JWT格式的令牌。项目通过Spring Security进行用户认证和授权，并支持OpenID Connect 1.0。使用Nimbus库生成并管理RSA密钥对，并在内存中注册客户端和用户。

## 技术栈
- **框架**: Spring Security, Spring Authorization Server
- **OAuth2授权**: 支持Authorization Code、Client Credentials和Refresh Token等授权方式
- **JWT支持**: 使用RSA密钥生成JWT令牌
- **用户与客户端管理**: 使用In-Memory方式管理用户和OAuth2客户端

## 功能
1. **OAuth2 授权服务器**：项目实现了OAuth2授权服务器，支持多种授权类型，如授权码模式、客户端凭证模式等。
2. **JWT支持**：使用RSA密钥对生成和验证JWT令牌，确保安全性。
3. **OpenID Connect**：支持OIDC（OpenID Connect 1.0），提供身份验证信息。
4. **用户管理**：通过内存存储的方式，配置了一些预定义的用户，支持基础的用户身份验证。
5. **客户端注册**：支持在内存中注册OAuth2客户端，配置了授权范围和重定向URI等信息。

## 安装步骤
1. 克隆项目到本地:
   ```bash
   git clone https://github.com/SaulGoodman-jl/spring-6-auth-server.git
   ```
2. 运行项目:
   ```bash
   .\mvnw spring-boot:run
   ```

## 配置说明
- 默认的JWT生成密钥对通过RSA算法生成，密钥保存在应用启动时自动生成的`KeyPair`对象中。
- 项目使用内存存储用户和客户端配置，示例用户为：
    - 用户名：`user`
    - 密码：`password`

## License
该项目基于MIT许可证，请参阅[LICENSE](./LICENSE)文件获取更多信息。