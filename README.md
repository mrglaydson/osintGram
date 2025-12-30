# osintGram

Descrição simples do projeto: ferramenta de OSINT para investigar perfis públicos do Instagram usando uma Session ID válida.

---

## 🔧 Requisitos

- **Python 3.8+** instalado
- Biblioteca Python: `requests`

Instale a dependência com:

```bash
pip install requests
```

---

## 🚀 Como executar

### Modo interativo (recomendado)

Execute o script sem parâmetros e siga o menu interativo:

```bash
python3 osintgram.py
# ou, se o arquivo for executável:
chmod +x osintgram.py
./osintgram.py
```

O modo interativo permite inserir o `username` e o `sessionid` diretamente, além de exportar os resultados ao final.

### Modo linha de comando (não interativo)

- Mostrar tutorial de como obter o Session ID:

```bash
python3 osintgram.py --tutorial
```

- Investigar um usuário e exportar os dados (exemplo JSON):

```bash
python3 osintgram.py -u <username> -s '<SESSIONID>' -o resultado -f json
```

- Opções principais:
  - `-u`, `--username` — username do Instagram (sem `@`)
  - `-s`, `--sessionid` — Session ID do Instagram (obtenha via cookies do navegador)
  - `-o`, `--output` — nome do arquivo de saída (sem extensão)
  - `-f`, `--format` — `json` ou `csv` (padrão: `json`)

> Observação: se não for passado `--output`, o script pode perguntar se deseja exportar e, quando exportado, usará um nome no formato `instagram_<username>_<timestamp>.<ext>` salvo no diretório atual.

---

## ⚠️ Segurança e ética

- **Mantenha seu `sessionid` em sigilo**; ele fornece acesso associado à sua sessão no Instagram.
- Use esta ferramenta apenas para fins legais e éticos — **não** para invadir privacidade, assediar ou violar termos de serviço.
- O autor não se responsabiliza por uso indevido.

---

## 🛠️ Solução de problemas

- Se ocorrer erro de *rate limit* ou resposta inválida, tente novamente mais tarde.
- Verifique sua conexão de rede e confirme que o `sessionid` é válido e vigente.
- Em caso de erro ao exportar, verifique permissões de escrita no diretório atual.

---

## ✉️ Contato / Contribuição

Abra uma *issue* ou PR no repositório para sugestões, correções ou melhorias.

---

**Boa investigação!** 🔍
