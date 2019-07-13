## Melhorando o Script - parte 1

- *em breve*

### Pontos

- Separar as coisas em funções
- Mover o script do enter para um segundo arquivo
- Verificar se o arquivo foi realmente passado
- Normalizar os caminhos para caminho absoluto
- Verificar se a pasta do source existe
- Verificar se o source existe
- Reorganizar o script colocando a função main como primeira coisa

### Snippets

- Normalizar caminho da pasta para caminho absoluto

```bash
function normalize_source_path_to_absolute()
{
  local relative_folder

  relative_folder=$(dirname "$1")

  if cd "$relative_folder" 2> /dev/null
  then
    declare -gr "SOURCE_DIR=$(pwd)"
  else
    echo -e '\nERROR'
    echo -e "   $relative_folder doesn't exist!"
    exit 1
  fi

  declare -gr "SOURCE_PATH=$SOURCE_DIR/$(basename "$1")"
}
```

- Garantir que um arquivo existe

```bash
function ensure_file_exists()
{
  if [ ! -f "$1" ]
  then
    echo -e '\nERROR'
    echo -e "   $1 doesn't exist!"
    exit 1
  fi
}
```

### Código final
