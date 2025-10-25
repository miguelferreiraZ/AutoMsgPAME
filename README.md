# AutoMsgPAME

Sistema automático de envio de mensagens via WhatsApp para processos seletivos do PAME.

## Funcionalidades

- Envio automático de mensagens personalizadas via WhatsApp Web
- Sistema de checkpoint/resume (continua de onde parou se interrompido)
- Log detalhado de envios
- Estimativa de tempo de envio
- Tratamento robusto de erros
- Fechamento automático de abas

## Requisitos

```bash
pip install pandas pywhatkit pyautogui
```

## Configuração

Edite as variáveis no arquivo `main.py`:

- `ARQUIVO_PLANILHA`: Caminho do arquivo CSV/Excel com os contatos
- `COLUNA_TELEFONE`: Nome da coluna com os números de telefone
- `COLUNA_NOME`: Nome da coluna com os nomes (opcional)
- `MENSAGEM`: Mensagem a ser enviada (use {nome} para personalizar)
- `TEMPO_ESPERA`: Tempo entre mensagens (recomendado: 20 segundos)

## Como Usar

1. Certifique-se de que o WhatsApp Web está aberto e conectado
2. Execute o script:
   ```bash
   python main.py
   ```
3. Pressione ENTER quando solicitado
4. O script enviará as mensagens automaticamente

## Recursos

- **Progresso salvo**: Se interromper (Ctrl+C ou erro), o progresso é salvo em `progresso_envio.json`
- **Log de envios**: Histórico completo em `log_envios.txt`
- **Retomada**: Execute novamente o script para continuar de onde parou

## Observações

- Tempo estimado para 300 mensagens: ~1h 55min
- Progresso é salvo a cada 5 mensagens
- Em caso de erro, aguarda 10 segundos antes de continuar
- As abas do WhatsApp são fechadas automaticamente após cada envio

## Autor

Miguel Ferreira
