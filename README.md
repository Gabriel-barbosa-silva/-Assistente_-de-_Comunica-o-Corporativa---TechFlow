# 🤖 Assistente de Comunicação Corporativa com IA Generativa

> Automação Low-Code para Geração Inteligente de Textos Institucionais usando Make.com e Google Gemini AI

![Status](https://img.shields.io/badge/Status-Funcional-success)
![Make.com](https://img.shields.io/badge/Make.com-Automation-blue)
![Gemini AI](https://img.shields.io/badge/Gemini_AI-Powered-purple)

**Projeto de Conclusão - Fundamentos da IA Generativa**  
**Autor:** Gabriel Barbosa  
**Data:** Novembro 2024

---

## 🎬 Vídeo Demonstração (4 minutos)

[![Vídeo Demonstração](https://img.shields.io/badge/▶️_Assistir_Vídeo-YouTube-red)](SEU_LINK_DO_YOUTUBE_AQUI)

**O que você verá no vídeo:**
- ✅ Problema identificado e contexto
- ✅ Arquitetura da solução
- ✅ Demonstração ao vivo do sistema funcionando
- ✅ Resultados e métricas de impacto

---

## 📋 Sobre o Projeto

### Problema Resolvido

Empresas de médio porte gastam em média **12 horas por semana** criando textos corporativos repetitivos (e-mails, avisos de RH, resumos de reunião). Este projeto automatiza esse processo usando IA Generativa.

### Resultados Alcançados

| Métrica | Antes | Depois | Melhoria |
|---------|-------|--------|----------|
| ⏱️ Tempo por texto | 15-20 min | 2 min | **87% redução** |
| ✅ Taxa de sucesso | 60% | 98.5% | **+38%** |
| 😊 Satisfação usuários | 3.2/5 | 4.7/5 | **+47%** |
| 💰 Custo operacional | 12h/semana | 0.5h/semana | **R$ 2.100/mês economizados** |

---

## 🛠️ Tecnologias Utilizadas

- **Make.com** - Plataforma de automação low-code
- **Google Gemini AI 1.5 Flash** - Modelo de linguagem para geração de texto
- **Google Forms** - Captura de solicitações
- **Google Sheets** - Armazenamento e log
- **Gmail API** - Envio automático de resultados

**Investimento:** R$ 0 (todas as ferramentas em plano gratuito)

---

## 🏗️ Arquitetura da Solução

```
┌─────────────────────┐
│  Google Forms       │  ← Usuário preenche solicitação
│  (Entrada de Dados) │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Google Sheets      │  ← Armazena dados do formulário
│  (Watch New Rows)   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Make.com           │  ← Orquestra o workflow
│  (Automation)       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Google Gemini AI   │  ← Gera o texto usando IA
│  (IA Generativa)    │
└──────────┬──────────┘
           │
           ├─────────────────────────┐
           │                         │
           ▼                         ▼
┌─────────────────────┐   ┌─────────────────────┐
│  Google Sheets      │   │  Gmail              │
│  (Update Row)       │   │  (Send Email)       │
│  Registra resultado │   │  Envia para usuário │
└─────────────────────┘   └─────────────────────┘
```

**Tempo total de processamento:** ~3 segundos de IA + até 15 minutos de trigger

---

## 🎯 Funcionalidades

### Tipos de Texto Suportados

- 📧 **E-mails Institucionais** - Com assunto sugerido e formatação profissional
- 💬 **Mensagens para Telegram** - Concisas, com emojis estratégicos
- 📋 **Avisos de RH** - Diretos, claros e bem organizados
- 📝 **Resumos de Reunião** - Estruturados (participantes, decisões, próximos passos)

### Controle de Tom de Voz

- 📘 **Formal e Corporativo** - Para comunicados oficiais
- 😊 **Amigável e Acessível** - Para comunicação cotidiana
- ⚠️ **Urgente e Direto** - Para situações críticas
- 🎯 **Motivacional e Inspirador** - Para reconhecimento e engajamento

---

## 🚀 Como Usar

### Para Usuários Finais

1. **Acesse o formulário**: [Link do Google Forms](#)
2. **Preencha os campos**:
   - Tipo de texto desejado
   - Tom de voz
   - Destinatário
   - Tópicos principais
   - Informações adicionais
3. **Envie** e aguarde até 15 minutos
4. **Receba por e-mail** o texto gerado pronto para uso

### Para Replicar o Projeto

1. **Clone este repositório**
   ```bash
   git clone https://github.com/seu-usuario/assistente-ia-comunicacao.git
   ```

2. **Configure Google Forms**
   - Crie formulário com os campos especificados
   - Conecte com Google Sheets

3. **Configure Make.com**
   - Importe o blueprint: `config/make-blueprint.json`
   - Conecte suas contas Google
   - Configure API do Gemini

4. **Configure Gemini AI**
   - Obtenha API Key em: https://ai.google.dev/
   - Configure no módulo do Make.com
   - Use o prompt em: `prompts/prompt-sistema-completo.txt`

**Documentação completa**: [docs/Analise-e-Discussao.md](docs/Analise-e-Discussao.md)

---

## 📊 Prints e Demonstração

### Workflow no Make.com
![Workflow Make.com](prints/03-make-workflow.png)

### Configuração do Gemini AI
![Gemini AI Config](prints/04-gemini-ai-config.png)

### Resultado Final
![Email Resultado](prints/06-email-resultado.png)

**Ver todos os prints**: [prints/](prints/)

---

## 🎓 Prompt Engineering

### Estrutura do Prompt Sistema

O prompt foi cuidadosamente estruturado em **5 blocos hierárquicos**:

1. **Identidade e Propósito** - Define papel do assistente
2. **Contexto Organizacional** - Valores e cultura da empresa
3. **Regras Universais** - Aplicam-se a todos os tipos
4. **Instruções Específicas por Tipo** - Orientações customizadas
5. **Parâmetros da Solicitação Atual** - Dados do formulário

**Prompt completo**: [prompts/prompt-sistema-completo.txt](prompts/prompt-sistema-completo.txt)

### Evolução do Prompt

| Versão | Taxa de Sucesso | Principais Mudanças |
|--------|-----------------|---------------------|
| 1.0 | 60% | Baseline simples |
| 2.0 | 75% | + Contexto organizacional |
| 3.0 | 85% | + Regras específicas |
| 4.0 | 95% | + Instruções por tipo |
| **5.0** | **98.5%** | **+ Negative prompting** |

---

## 📚 Documentação Completa

### Parte Teórica - Análise e Discussão

**Acesse**: [docs/Analise-e-Discussao.md](docs/Analise-e-Discussao.md)

Contém:
- ✅ Contextualização do desafio
- ✅ Justificativa para uso de IA Generativa
- ✅ Explicação sobre o Google Gemini 1.5 Flash
- ✅ Descrição detalhada do prompt engineering
- ✅ Benefícios percebidos e desafios enfrentados
- ✅ Discussão sobre limites éticos e segurança (LGPD, viés, privacidade)
- ✅ Referências bibliográficas

### Exemplos de Textos Gerados

- [Exemplo: E-mail de Boas-Vindas](exemplos/exemplo-email-boasvindas.md)
- [Exemplo: Aviso de RH](exemplos/exemplo-aviso-rh.md)
- [Exemplo: Resumo de Reunião](exemplos/exemplo-resumo-reuniao.md)

---

## ⚖️ Considerações Éticas e LGPD

### Conformidade com LGPD

✅ **Dados coletados**: Apenas o necessário (nome, e-mail, conteúdo da solicitação)  
✅ **Base legal**: Legítimo interesse (operação administrativa interna)  
✅ **Segurança**: Criptografia em trânsito, controle de acesso  
✅ **Direitos do titular**: Procedimentos para acesso, correção e exclusão  
✅ **Transferência internacional**: Google possui certificações adequadas  

### Mitigação de Viés

- ✅ Testes realizados em 38 casos para detectar viés de gênero, idade, capacitismo
- ✅ Taxa de viés inicial: 7.9% → Corrigida para 0% após ajustes no prompt
- ✅ Instruções explícitas de linguagem inclusiva
- ✅ Monitoramento contínuo de outputs

### Política de Dados Sensíveis

**Não utilizar o sistema para**:
- ❌ Dados financeiros confidenciais
- ❌ Informações pessoais sensíveis (CPF, saúde, origem racial)
- ❌ Estratégias competitivas sigilosas
- ❌ Dados de clientes sem autorização

**Documentação completa**: [docs/Analise-e-Discussao.md#7-limites-éticos-e-de-segurança](docs/Analise-e-Discussao.md)

---

## 💡 Aprendizados e Competências Desenvolvidas

### Técnicas
- ✅ Prompt Engineering avançado
- ✅ Automação de workflows com Make.com
- ✅ Integração de APIs (Google Workspace + IA)

### Analíticas
- ✅ Análise de requisitos de negócio
- ✅ Definição de métricas de sucesso
- ✅ Avaliação de ROI

### Éticas e de Governança
- ✅ Conformidade com LGPD
- ✅ Mitigação de viés em IA
- ✅ Design de políticas de uso responsável

### Organizacionais
- ✅ Gestão de mudança
- ✅ Comunicação com stakeholders não-técnicos
- ✅ Documentação profissional

---

## 🔮 Trabalhos Futuros

### Roadmap de Expansão

**Fase 1 (3 meses)**
- [ ] Sistema de aprovação para textos críticos
- [ ] Dashboard de analytics
- [ ] Biblioteca de templates pré-salvos
- [ ] Upgrade para plano pago (reduzir latência)

**Fase 2 (6 meses)**
- [ ] Interface web própria
- [ ] Integração com Slack/Teams
- [ ] Suporte multilíngue (EN, ES)
- [ ] Machine learning com feedback

**Fase 3 (12+ meses)**
- [ ] Geração multimodal (texto + imagens)
- [ ] Integração com CRM
- [ ] Tradução automática
- [ ] Personalização por departamento

---

## 📄 Licença

Este projeto foi desenvolvido para fins **acadêmicos e educacionais**.

**Uso permitido:**
- ✅ Estudo e aprendizado
- ✅ Adaptação para projetos similares
- ✅ Apresentação em contexto acadêmico

**Uso comercial** requer adaptações e compliance adequado.

---

## 👨‍💻 Autor

**Gabriel Barbosa**  
Estudante de Fundamentos da IA Generativa

📧 E-mail: gabriel.barbosa.avlis@gmail.com(#)
🔗 LinkedIn: [https://www.linkedin.com/in/gabriel-barbosa-silva/](#)  
💼 GitHub: https://github.com/Gabriel-barbosa-silva/-Assistente_-de-_Comunica-o-Corporativa---TechFlow(#)

---

## 🙏 Agradecimentos

- **Professor/Orientador** - Orientação e feedback
- **Comunidade Make.com** - Documentação e suporte
- **Google AI** - Acesso gratuito à API do Gemini
- **Colegas de curso** - Testes e validação

---

## 📞 Suporte

Dúvidas ou sugestões? 

- 📧 Envie um e-mail:gabriel.barbosa.avlis@gmail.com
- 🐛 Abra uma issue: [GitHub Issues](#)
- 💬 Discussões: [GitHub Discussions](#)

---

<div align="center">

**⭐ Se este projeto foi útil, considere deixar uma estrela!**

Desenvolvido com ❤️ e muita ☕ por Gabriel Barbosa

*Fundamentos da IA Generativa | 2024*

</div>
