# Principais comandos `chmod` para concursos

O `chmod` (*change mode*) é um comando do Linux utilizado para alterar as permissões de arquivos e diretórios.

## 1. Tabela de permissões

| Permissão | Letra | Valor |
|---|---|---:|
| Leitura (*read*) | `r` | 4 |
| Escrita (*write*) | `w` | 2 |
| Execução (*execute*) | `x` | 1 |
| Nenhuma permissão | `-` | 0 |

Os valores são somados para formar cada grupo de permissões.

| Valor | Permissões | Significado |
|---:|---|---|
| `0` | `---` | Nenhuma permissão |
| `1` | `--x` | Somente execução |
| `2` | `-w-` | Somente escrita |
| `3` | `-wx` | Escrita e execução |
| `4` | `r--` | Somente leitura |
| `5` | `r-x` | Leitura e execução |
| `6` | `rw-` | Leitura e escrita |
| `7` | `rwx` | Leitura, escrita e execução |

**Macete:** `r = 4`, `w = 2` e `x = 1`. Portanto, `rwx = 4 + 2 + 1 = 7`.

## 2. Principais comandos numéricos

| Comando | Permissões resultantes | Interpretação |
|---|---|---|
| `chmod 777 arquivo` | `rwxrwxrwx` | Todos têm todas as permissões |
| `chmod 755 arquivo` | `rwxr-xr-x` | Dono tem tudo; grupo e outros leem e executam |
| `chmod 700 arquivo` | `rwx------` | Somente o dono tem permissões |
| `chmod 644 arquivo` | `rw-r--r--` | Dono lê e escreve; grupo e outros só leem |
| `chmod 666 arquivo` | `rw-rw-rw-` | Todos leem e escrevem |
| `chmod 600 arquivo` | `rw-------` | Somente o dono lê e escreve |
| `chmod 640 arquivo` | `rw-r-----` | Dono lê e escreve; grupo só lê |
| `chmod 444 arquivo` | `r--r--r--` | Todos somente leem |
| `chmod 400 arquivo` | `r--------` | Somente o dono lê |
| `chmod 000 arquivo` | `---------` | Nenhuma permissão para os três grupos |

### Como interpretar `chmod 754 arquivo`?

Os três dígitos representam, nesta ordem:

1. **Dono (*user*):** `7` = `rwx` (leitura, escrita e execução).
2. **Grupo (*group*):** `5` = `r-x` (leitura e execução).
3. **Outros (*others*):** `4` = `r--` (somente leitura).

Resultado: `rwxr-xr--`.

## 3. Comandos com letras (modo simbólico)

| Símbolo | Representa |
|---|---|
| `u` | Dono (*user*) |
| `g` | Grupo (*group*) |
| `o` | Outros (*others*) |
| `a` | Todos (*all*) |
| `+` | Adiciona permissões |
| `-` | Remove permissões |
| `=` | Define exatamente as permissões indicadas |

### Exemplos

| Comando | Efeito |
|---|---|
| `chmod u+x arquivo` | Adiciona execução para o dono |
| `chmod g+w arquivo` | Adiciona escrita para o grupo |
| `chmod o-r arquivo` | Remove leitura de outros |
| `chmod a+x arquivo` | Adiciona execução para todos |
| `chmod u=r arquivo` | Define somente leitura para o dono |
| `chmod go-w arquivo` | Remove escrita do grupo e de outros |
| `chmod u+x,g-w arquivo` | Adiciona execução ao dono e remove escrita do grupo |
| `chmod -x arquivo` | Remove execução de todos |

**Pegadinha:** `chmod u=r arquivo` substitui as permissões anteriores do dono pelas indicadas. Já `chmod u+r arquivo` apenas adiciona leitura.

## 4. Diferença entre permissões em arquivos e diretórios

| Permissão | Em arquivos | Em diretórios |
|---|---|---|
| `r` — leitura | Ler o conteúdo | Listar os nomes dos itens |
| `w` — escrita | Modificar o conteúdo | Criar, excluir e renomear itens, dependendo das demais permissões |
| `x` — execução | Executar o arquivo, se aplicável | Acessar e atravessar o diretório |

**Atenção:** em um diretório, a permissão `w` sem `x` normalmente não permite realizar operações úteis de criação, remoção ou renomeação de itens.

## 5. Comandos adicionais importantes

| Comando | O que faz |
|---|---|
| `chmod -R 755 pasta/` | Aplica as permissões recursivamente à pasta e aos itens abaixo dela |
| `chmod +x script.sh` | Adiciona execução para todos |
| `chmod -x script.sh` | Remove execução de todos |
| `chmod 644 arquivo.txt` | Define permissões numéricas para um arquivo |
| `chmod 755 diretorio/` | Define permissões numéricas para um diretório |

O parâmetro `-R` significa *recursive* (recursivo). Ele aplica a alteração à árvore de diretórios e aos itens contidos nela.

## 6. Resumo para revisão

Priorize os seguintes conteúdos para concursos:

1. Valores: `r = 4`, `w = 2`, `x = 1`.
2. Conversão entre valores numéricos e permissões simbólicas.
3. Permissões mais comuns: `755`, `644`, `700`, `600` e `777`.
4. Ordem dos grupos: **dono → grupo → outros**.
5. Operadores simbólicos: `+`, `-` e `=`.
6. Parâmetro `-R`: alteração recursiva.
7. Diferenças entre permissões de arquivos e diretórios.

### Macete final

- `755` → dono faz tudo; grupo e outros leem e executam.
- `644` → dono lê e escreve; grupo e outros só leem.
- `700` → somente o dono tem permissões.
- `600` → somente o dono lê e escreve.
- `777` → todos têm todas as permissões.

**Regra fundamental:** os três dígitos do `chmod` representam, respectivamente, as permissões do dono, do grupo e dos outros.