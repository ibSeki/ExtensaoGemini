# Extensao-Gemini

```markdown
# 🎓 ExtensaoGemini

Uma aplicação backend que utiliza a API do Gemini para extrair os **principais tópicos** de vídeos educacionais do YouTube. Ideal para estudantes, pesquisadores e criadores de conteúdo que desejam um resumo rápido e inteligente dos vídeos assistidos.

## 🚀 Funcionalidades

- 🔗 Baixa o áudio de vídeos do YouTube  
- 🧠 Transcreve automaticamente o conteúdo utilizando a API AssemblyAI  
- 💡 Identifica os 7 principais tópicos abordados com a IA Gemini  
- 🧪 Retorna um JSON estruturado com os tópicos para uso em extensões ou aplicações externas

## 🛠️ Tecnologias Utilizadas

- Python 3  
- Flask + Flask-CORS  
- API AssemblyAI (transcrição)  
- API Gemini (Google) – análise de tópicos  
- dotenv (para gerenciamento da chave da API)  
- youtube_dl (para baixar áudio do YouTube)

## 📁 Estrutura do Projeto

```
ExtensaoGemini/
├── Back/
│   ├── main.py              # Endpoint principal para processar vídeos
│   ├── transcricao.py       # Transcrição de áudio com AssemblyAI
│   ├── topicos.py           # Análise com API Gemini
├── Front/
│   └── icon.png             # Ícone da extensão (se aplicável)
├── .gitignore
├── README.md
```

## 📦 Como Executar Localmente

1. Clone este repositório:
   ```bash
   git clone https://github.com/ibSeki/ExtensaoGemini.git
   cd ExtensaoGemini/Back
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Crie um arquivo `.env` com a sua chave da API Gemini:
   ```
   API_KEY_GEMINI=sua_chave_aqui
   ```

4. Execute o servidor Flask:
   ```bash
   python main.py
   ```

5. Faça uma requisição POST para `http://localhost:5000/process` com:
   ```json
   {
     "video_url": "https://youtube.com/...",
     "language": "pt",
     "num_topicos": 7
   }
   ```

## 📩 Contato

Desenvolvido por **Ian de Barros Seki**  
📧 ian.dbseki@gmail.com  
🔗 [GitHub - ibSeki](https://github.com/ibSeki)
```
