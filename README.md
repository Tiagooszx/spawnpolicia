# 🚓 Sistema de Spawn Policia - Brasil RP

Sistema web otimizado para gerenciar spawns de veículos policiais e coordenadas do servidor Brasil Roleplay.

## 🎯 Funcionalidades

- ✅ Listagem de veículos policiais com filtros por guarnição
- ✅ Sistema de coordenadas de locais importantes
- ✅ Busca em tempo real
- ✅ Cópia rápida de spawns e coordenadas
- ✅ **NOVO:** Exibição de imagens dos veículos
- ✅ Interface responsiva e otimizada
- ✅ Design moderno com animações suaves

## 📸 Como Adicionar Imagens dos Veículos

### Método 1: Imagens Locais
1. Crie uma pasta `asset/vehicles/` no diretório do projeto
2. Adicione as imagens dos veículos nesta pasta (formatos: jpg, png, webp)
3. No arquivo `vehicles.json`, adicione o campo `imagem` com o nome do arquivo:

```json
{
  "carro": "CAVEIRÃO Civil",
  "spawn": "wrstorm",
  "guarnicao": "PCESP",
  "imagem": "caveirao.jpg"
}
```

### Método 2: URLs Externas
Você pode usar URLs diretas de imagens hospedadas online:

```json
{
  "carro": "BMW Civil",
  "spawn": "rvm3rpm",
  "guarnicao": "PCESP",
  "imagem": "https://exemplo.com/imagens/bmw-policia.jpg"
}
```

### Imagem Padrão
- Se um veículo não tiver o campo `imagem`, será exibida a imagem padrão (`asset/policia.png`)
- Se a imagem especificada não for encontrada, também usa a imagem padrão

## 🛠️ Melhorias Implementadas

### Arquitetura do Código
- **Modularização:** Código separado em módulos específicos (AppState, DataLoader, FilterManager, etc.)
- **Padrão de Projeto:** Uso de Module Pattern e Revealing Module Pattern
- **Separação de Responsabilidades:** Cada módulo tem uma função específica

### Performance
- **Carregamento Paralelo:** Arquivos JSON carregados simultaneamente com `Promise.all`
- **Lazy Loading:** Imagens carregadas sob demanda
- **Escape de HTML:** Prevenção de XSS com sanitização de dados
- **Event Delegation:** Melhor gerenciamento de eventos

### Segurança
- Escape de caracteres especiais em HTML
- Validação de URLs de imagens
- Tratamento de erros robusto

### UX/UI
- Imagens dos veículos com hover effects
- Animações suaves e responsivas
- Loading states para imagens
- Fallback para imagens não encontradas

## 📁 Estrutura de Arquivos

```
spawnpolicia/
├── index.html              # Arquivo principal (refatorado)
├── styles.css              # Estilos mantendo cores originais
├── vehicles.json           # Dados dos veículos
├── coordinates.json        # Dados das coordenadas
├── asset/
│   ├── policia.png        # Logo e imagem padrão
│   └── vehicles/          # Pasta para imagens dos veículos (criar)
│       ├── caveirao.jpg
│       ├── bmw.jpg
│       └── ...
└── README.md              # Este arquivo
```

## 🎨 Cores Mantidas

O sistema mantém o esquema de cores original:
- **Fundo Principal:** #232eaa (azul royal)
- **Destaque:** #4caf50 (verde)
- **Secundário:** #2196f3 (azul claro)
- **Alerta:** #ffc107 (amarelo/dourado)

## 🚀 Como Usar

1. Abra o arquivo `index.html` em um navegador
2. Use as abas para alternar entre Veículos e Coordenadas
3. Use os filtros para selecionar guarnições específicas
4. Digite na busca para filtrar resultados
5. Clique no botão 📋 para copiar o spawn/coordenada

## 📝 Editando os Dados

### Adicionar Novo Veículo
Edite `vehicles.json`:
```json
{
  "carro": "Nome do Veículo",
  "spawn": "codigo_spawn",
  "guarnicao": "PCESP",
  "imagem": "nome-arquivo.jpg"
}
```

### Adicionar Nova Coordenada
Edite `coordinates.json`:
```json
{
  "local": "Nome do Local",
  "coordenada": "x,y,z"
}
```

## 🔧 Tecnologias Utilizadas

- HTML5 Semântico
- CSS3 com Flexbox e Grid
- JavaScript Vanilla (ES6+)
- Módulos JavaScript
- Async/Await
- Fetch API
- Clipboard API

## 📱 Responsividade

O sistema é totalmente responsivo e funciona perfeitamente em:
- 💻 Desktop
- 📱 Smartphones
- 📱 Tablets

## ⚡ Performance

- Carregamento otimizado de recursos
- Lazy loading de imagens
- Código minificado logicamente
- Sem dependências externas
- Leve e rápido

## 🎯 Próximas Melhorias Sugeridas

- [ ] Sistema de favoritos
- [ ] Exportação de dados
- [ ] Modo escuro
- [ ] Cache offline
- [ ] Categorias personalizadas
- [ ] Upload de imagens via interface

---

**Desenvolvido para Brasil Roleplay** 🇧🇷
