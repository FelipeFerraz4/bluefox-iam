# Blue Fox IAM (Identity and Access Management)

Repositório centralizado de autenticação e autorização baseado em **Keycloak**.

## 🚀 Como rodar
1. Crie a rede compartilhada (se ainda não existir):
   `docker network create shared-net`
2. Suba o ambiente:
   `docker-compose --env-file .env up -d`
3. Acesse em: `http://localhost:8080/auth`

## ⚙️ Configuração Inicial Recomendada
- **Realm:** `BlueFox`
- **Clients:**
    - `aquarismo-web`: (Public - Next.js/Angular)
    - `aquarismo-api`: (Confidential - Spring Boot)
- **Roles:**
    - `ROLE_ADMIN`: Acesso total ao blog e dashboards.
    - `ROLE_USER`: Acesso a conteúdos exclusivos.