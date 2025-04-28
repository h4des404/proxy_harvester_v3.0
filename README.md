# 🕵️‍♂️ Elite Proxy Harvester v3.0 — 404Group Intelligence Edition

Uma poderosa ferramenta para **raspagem, validação** e **filtragem de proxies** (HTTP, SOCKS4 e SOCKS5) em larga escala, focada em desempenho e eficiência.

---

## 🚀 Funcionalidades

- 🔎 **Raspagem de proxies** de múltiplas fontes públicas (mais de 20 sites).
- ⚡ **Validação automática** de proxies (testa a funcionalidade e anonimato real).
- 🌎 **Filtragem por país** usando códigos ISO (ex.: `US`, `BR`, `FR`, etc).
- 🧹 **Separacão automática** dos proxies por tipo (HTTP, SOCKS4, SOCKS5).
- 📄 **Exportação de resultados** em formatos `.txt`, `.json`, `.csv` e para `proxychains.conf`.
- 🌐 **Resolução de hostname** do IP, mostrando informações extras.
- 📋 **Exemplos de como utilizar os proxies** no `curl`, `Firefox`, `Python`, `Burp Suite`, etc.
- 🎨 Interface CLI colorida usando **Colorama**.

---

## 📁 Estrutura dos Arquivos Gerados

- `valid_proxies_TIMESTAMP.txt`: Todos os proxies válidos (todos os tipos misturados).
- `valid_http_TIMESTAMP.txt`: Somente proxies HTTP válidos.
- `valid_socks4_TIMESTAMP.txt`: Somente proxies SOCKS4 válidos.
- `valid_socks5_TIMESTAMP.txt`: Somente proxies SOCKS5 válidos.
- `valid_proxies_TIMESTAMP.json`: Arquivo JSON estruturado.
- `valid_proxies_TIMESTAMP.csv`: Arquivo CSV (excelente para análise ou manipulação).
- `proxychains.conf`: Arquivo pronto para uso no `proxychains`.

---

## 🛠 Pré-requisitos

Antes de rodar, você precisa ter instalado:

- **Python** 3.7 ou superior
- **pip** (gerenciador de pacotes do Python)
- **Git** (para clonar o repositório)
- **Git LFS** (Large File Storage) para arquivos grandes

### Bibliotecas Python necessárias

```bash
pip install -r requirements.txt
```

Ou, se quiser instalar manualmente:

```bash
pip install requests beautifulsoup4 pandas colorama
```

---

## 📥 Como instalar e executar

### 1. Instalar o Git LFS (se ainda não tiver)

- **Windows**: [Instalador Oficial Git LFS](https://git-lfs.github.com/)
- **Linux/macOS**:

```bash
sudo apt install git-lfs
git lfs install
```

### 2. Clonar o repositório

```bash
git clone https://github.com/h4des404/proxy_harvester_v3.0.git
cd proxy_harvester_v3.0
```

---

## ▶️ Como executar a ferramenta

Basta rodar:

```bash
./proxy_harvester_v3.0
```

> Obs.: Pode ser necessário dar permissão de execução no Linux/Mac:

```bash
chmod +x proxy_harvester_v3.0
./proxy_harvester_v3.0
```

---

## 🎮 Menu Principal

Quando iniciar, você verá o menu:

```text
1. Raspagem + Validação (HTTP, SOCKS4, SOCKS5)
2. Mostrar como usar proxies
3. Sair
```

- **Opção 1**: Escolha o número de threads (ex.: 100) e se deseja filtrar proxies por país.
- **Opção 2**: Dicas de como configurar os proxies nos seus programas.
- **Opção 3**: Sair da ferramenta.

---

## 💬 Exemplos de Uso dos Proxies

- **No `curl`**:

```bash
curl -x socks5://IP:PORT https://example.com
```

- **No Burp Suite**:
  - Vá em Proxy → Options → Add SOCKS/HTTP Proxy

- **No Firefox**:
  - Acesse `about:config` → Pesquise por `network.proxy.*` → Configure.

- **Em Python**:

```python
proxies = {
    "http": "socks5://IP:PORT",
    "https": "socks5://IP:PORT"
}
response = requests.get("https://example.com", proxies=proxies)
```

- **Usando Proxychains (Linux/Mac)**:
  - Arquivo `proxychains.conf` já é gerado pronto para usar.

---

## ⚡ Recomendações

- Utilize **50 a 150 threads** para melhor desempenho (pode variar conforme seu PC e rede).
- Sempre use **VPN** ao testar proxies de fontes públicas.
- Atualize o repositório com frequência para pegar novas fontes de proxy.

---

## 🧐 Créditos

Projeto desenvolvido por **h4des404 | 404Group**  
💬 Para sugestões ou melhorias, abra uma `issue` ou mande uma `pull request`!

---

## ❤️ Agradecimentos

Gostaria de agradecer às tecnologias e às comunidades que tornaram este projeto possível:

**Python** - Linguagem de programação principal utilizada.

**Requests** - Para todas as requisições HTTP.

**BeautifulSoup4** - Para o parsing de HTML.

**Colorama** - Para adicionar cor no terminal.

**Pandas** - Para manipulação e exportação de dados.

**Git LFS** - Para gerenciar arquivos grandes no repositório.

---

## 📜 Licença

Este projeto é apenas para uso educacional e testes de segurança autorizados. Não nos responsabilizamos por usos indevidos. 
Licença **MIT** — veja o arquivo [LICENSE](LICENSE) para detalhes.

---

# 🚀 Let’s Harvest Some Proxies!

---

