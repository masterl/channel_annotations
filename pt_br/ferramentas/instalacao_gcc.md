## Instalação do GCC

-  https://www.youtube.com/watch?v=ntp4CpQoXzs

#### Nota:
***Os pacotes sugeridos para as distribuições de Linux instalam mais que o pacote GCC!***

São na verdade conjuntos de pacotes para compilação de programas.
Faço a sugestão de instalá-los, pois além de também instalarem o *make* que utilizarei em alguns vídeos, também são necessários para compilar algum programa do qual você tenha obtido o código-fonte na internet.

### Passos

- Linux
  - Debian/Ubuntu/Xubuntu/Kubuntu/Lubuntu
    - `sudo apt-get install build-essential`
  - Arch Linux/Manjaro(?)
    - pacote *base-devel*
  - Fedora
    - `yum groupinstall "Development Tools" "Development Libraries"`
- Windows
  1. Baixar o TDM-GCC http://tdm-gcc.tdragon.net
  2. Instalar
  3. Conferir se adicionou ao PATH
- MacOS
  1. Xcode
  2. Xcode > preferencias > downloads > "Command line tools" > install
