### Pipeline CI/CD GitHub Actions + Kubernetes + Docker + Docker Hub


### Pipeline de CI - Continuous Integration
- Disparada mediante o evento de um push no repositório do GitHub
- Checkout do novo código, build da imagem Docker e publicação dela no registry Docker Hub .

### Pipeline de CD - Continuous Delivery
- Execução condicionada ao sucesso da pipeline de CI
- Configurado o contexto para acesso ao cluster Kubernetes
- Deploy da imagem Docker no cluster Kubernetes


Em ambas as pipelines, foram definidos runners Linux Ubuntu.

Os dados de acesso ao Docker Hub e contexto Kubernetes foram armazenados em Secrets

Foram utilizadas actions do Marketplace para
- Login e Push das imagens no Docker Hub 
- Configurar contexto e efetuar deploy no cluster Kubernetes
