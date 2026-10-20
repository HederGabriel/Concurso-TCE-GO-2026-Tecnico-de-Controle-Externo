[← Voltar para a questão](Questões/systemctl%202022.md)
# `systemctl` — Revisão Rápida

## 1. Sintaxe

```bash
systemctl [opção] [unidade]
```

Exemplo:

```bash
systemctl reload cups.service
```

- `systemctl`: gerencia serviços pelo **systemd**.
- `reload`: solicita o recarregamento da configuração.
- `cups.service`: serviço relacionado à impressão no Linux (CUPS).
> CUPS = Common UNIX Printing System (Sistema Comum de Impressão Unix)

## 2. Principais opções

| Opção | Função |
|---|---|
| `start` | Iniciar o serviço |
| `stop` | Parar o serviço |
| `restart` | Reiniciar o serviço |
| `reload` | Recarregar a configuração |
| `status` | Consultar o estado |
| `enable` | Habilitar inicialização automática |
| `disable` | Desabilitar inicialização automática |

**Atenção:** `reload` ≠ `restart`. O primeiro recarrega a configuração; o segundo reinicia o serviço.

## 3. systemd × SysVinit

- **systemd:** utiliza `systemctl` para gerenciar serviços.
- **SysVinit:** associado tradicionalmente a scripts em `/etc/init.d/`.

## 4. Resolução da questão

- **I — Incorreta:** `systemctl` está associado ao systemd, não ao SysVinit.
- **II — Incorreta:** `reload` recarrega a configuração; para reiniciar, utiliza-se `restart`.

**Gabarito: C — as duas afirmativas estão incorretas.**