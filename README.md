# PowerApps-FontAwesomeIcons-Component
Componente criado para adicionar os ícones gratuitos do Font Awesome

## Conteúdo

- [Importando o componente](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Importando%20o%20componente.md)
- [Propriedades de entrada](#propriedades-de-entrada)
- [Propriedades de saída](#propriedades-de-saída)
- [Configuração inicial](#configuração-inicial)

### Propriedades de entrada

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Icon Style | IconStyle | Categoria de estilo da fonte | Texto | "" |
| Icon Name | IconName | Nome do ícone a ser usado | Texto | "" |
| Hex Color | HexColor | Valor hexadecimal da cor do ícone | Texto | "" |
| Cursor Type | CursorType | Tipo de cursor no mouseover | Número | 0 |
| OnSelect | OnSelect | Funções a serem executadas ao clicar no ícone | Função | "" |

### Propriedades de saída

| Nome de exibição | Propriedade | Descrição | Tipo de Dados | Default |
| - | - | - | - | - |
| Styles | Styles | Enum para ser usado na propriedade de entrada "Icon Style" | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/NotificationTypes.md) |
| Style Source | StyleSource | Texto com a fonte-face usada conforme a seleção do estilo (implícito) | Texto | "" |
| Version | Version | Exibe a versão do Font Awesome que está sendo usada | Texto | "fontawesome-free-6.4.0-desktop" |
| Cursor Types | CursorTypes | Enum para ser usado na propriedade de entrada "Cursor Type" | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/NotificationTypes.md) |
| Icons | Icons | Enum para ser usado na propriedade de entrada "Icon Name" | Registro | [ver registro](https://github.com/eduardoreisfernandes/Power-Apps-Toast-Notification-Component/blob/main/Registros/NotificationTypes.md) |
| Image | Image | Retorna a imagem do ícone configurado no componente, para ser usado em componentes de imagem no Power Apps | Imagem | "" |
| RenderIcon | RenderIcon | Retorna o ícone para ser usado em vários componentes de imagem, configurando os parâmetros individualmente | Texto | "" |

### Configuração inicial

1. O componente inicialmente ficará vazio, até que as propriedades necessárias sejam configuradas.

![image](https://user-images.githubusercontent.com/47257185/230199013-37a9f80b-3f8a-4e75-a03b-324ce7a38917.png)

2. As propriedades principais deverão ser preenchidas para visualizar o ícone. São elas: **_Icon Style_** e **_Icon Name_**. 

![image](https://user-images.githubusercontent.com/47257185/230199334-04cd3c57-27c7-446d-b427-ef6b25db9722.png)

- **Icon Style** indica o estilo de ícone entre as categorias filtradas no site Font Awesome. Na versão gratuita, são 3 tipos: 
  - **_Brands_**
  - **_Regular_**
  - **_Solid_**
  
Para facilitar a utilização, o componente possui uma propriedade de saída **_Styles_**, que é um Enum com todos os tipos possíveis para serem escolhidos. Exemplo:

```
Self.Styles.Brands
```

- **Icon_Name** indica qual é o ícone que será exibido na tela. Qualquer ícone listado como gratuito até a versão indicada no componente pode ser utilizado. Para facilitar o uso, o componente possui uma propriedade de saída **_Icons_**, que é um Enum com todos os nomes dos ícones possíveis. São mais de 2000 ícones e estão dividos pelos estilos já mencionados. 

```
Self.Icons.Brands.facebook
```

**OBS.:** é necessário que o **_Icon Style_** e o **_Icon Name_** sejam da mesma categoria, mesmo estilo, como no nosso exemplo acima, **_Brands_**. Se o estilo for alterado para **_Regular_**, por exemplo, é necessário também alterar no **_Icon name_** a referência do estilo.

3. A propriedade **Hex Color** pode ser preenchida para alterar a cor do ícone. Passe um valor em hexadecimal. Exemplo: "#0000ff".

4. A propriedade **Cursor Type** indica o tipo do cursor do mouse quando ele passar sobre o ícone. Por padrão, o valor é 0, indicando que o componente é clicável. A outra opção é -1, indicando o cursor normal. Para facilitar o uso, o componente possui uma propriedade de saída **_CursorTypes_**, que é um Enum com todos os tipos possíveis para serem escolhidos. Exemplo:

```
Self.CursorTypes.Pointer
```

5. A propriedade **OnSelect** é uma propriedade de comportamento. Indica qual função deverá ser executada ao clicar no componente. Apesar do tipo estar marcado como booleano, essa propriedade aceitará as funções que forem passadas nela.

![image](https://user-images.githubusercontent.com/47257185/230203536-a7632970-2978-4eac-b900-2c725aac81ea.png)
