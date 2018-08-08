## ??? - Objetos constantes com membro ponteiro

- *em breve*

### Pontos
- Mostrar que valores apontados podem ser alterados
  - Exemplo:


  ```cpp
  struct Teste
  {
    Teste ( int *original_addr ):
      numero_( original_addr )
    {
    };

    int *numero_;
  };

  int valor = 15;
  const Teste teste( &valor );

  *teste.numero_ = 32;

  std::cout << valor << std::endl;
  ```
