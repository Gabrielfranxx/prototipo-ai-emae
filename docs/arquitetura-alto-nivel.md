# 🏗️ Arquitetura em Alto Nível

A solução foi estruturada usando ferramentas no-code/low-code e APIs de IA para permitir criação rápida, testes e apresentação executiva.

---

## 🔄 Fluxo de Funcionamento

1. **Usuário envia mensagem pelo Microsoft Teams**  
   - Ponto de entrada principal.

2. **N8N recebe o evento e inicia o fluxo**  
   - Atua como orquestrador geral.

3. **A mensagem é enviada ao GPT-4o (OpenAI)**  
   - Interpretação da intenção.
   - Transformação da mensagem em embeddings.

4. **Armazenamento no banco da Supabase**  
   - Embeddings e histórico ficam disponíveis para consultas futuras.

5. **DeepSeek API realiza busca semântica**  
   - Relaciona mensagens novas com conhecimento armazenado.

6. **GPT-4o monta a resposta final**  
   - Usa dados recuperados + intenção atual do usuário.

7. **N8N envia a resposta de volta ao Microsoft Teams**  
   - Entrega final ao usuário.

---

## 🧩 Tecnologias Utilizadas

| Componente | Função |
|-----------|--------|
| **N8N** | Orquestração de todo o fluxo |
| **Microsoft Teams** | Interface de chat |
| **OpenAI GPT-4o** | Interpretação e geração de respostas |
| **DeepSeek API** | Busca semântica e enriquecimento |
| **Supabase** | Banco + armazenamento vetorial |
| **APIs internas** | Integrações operacionais do RH |

---

## 📦 Benefícios da Arquitetura

- Permitiu entrega **rápida** para apresentação executiva.
- Baixo custo inicial.
- Fácil de ajustar conforme feedback do RH.
- Viável para expansão posterior para um sistema robusto.
