# 🍔 Cardápio Digital & Delivery Web - Chapa Quente

Cardápio digital moderno, responsivo e interativo para lanchonete, inspirado fielmente na experiência do aplicativo **Yooga Delivery** (`delivery.yooga.app/chapa-quente/tabs/home`).

---

## 🚀 Como Visualizar o Cardápio

Basta dar um duplo clique no arquivo **`index.html`** para abrir o cardápio em qualquer navegador (Google Chrome, Edge, Firefox, celular, etc.). Não é necessário instalar nenhum servidor ou programa adicional!

---

## 🎨 Como Inserir a sua Logo Oficial

O sistema já vem com uma logo provisória profissional vetorizada (`assets/img/logo-placeholder.svg`). Quando você estiver pronto para inserir a sua própria logo:

### Opção 1 (Mais fácil - Substituição de arquivo):
1. Salve a sua imagem com o nome **`logo.png`** (ou `.jpg`) dentro da pasta **`assets/img/`**.
2. Abra o arquivo **`index.html`** no Bloco de Notas ou editor de código.
3. Procure por `assets/img/logo-placeholder.svg` (por volta da linha 47):
   ```html
   <img 
     id="store-logo" 
     class="store-logo-img" 
     src="assets/img/logo.png" 
     alt="Logo da Lanchonete" 
   />
   ```
4. Salve e recarregue a página no navegador.

### Opção 2 (Link / URL da internet):
Você também pode colar direto o link de uma imagem da internet no `src`:
```html
<img id="store-logo" class="store-logo-img" src="https://seusite.com/sua-logo.png" alt="Logo" />
```

---

## ⚙️ Como Alterar WhatsApp, Chave PIX e Nome da Loja

Abra o arquivo **`js/products.js`**. Logo no início você encontrará as configurações da lanchonete:

```javascript
const STORE_CONFIG = {
  name: "Chapa Quente",                         // Nome da Lanchonete
  slogan: "Procure qualidade, não preço.",      // Slogan / Frase
  whatsapp: "5592994904803",                    // Número que vai receber os pedidos (DDI + DDD + Número)
  whatsappDisplay: "(92) 99490-4803",          // Número visível na tela
  pixKey: "(92) 99490-4803",                    // Sua chave PIX
  pixName: "Ana Silva",                         // Titular da conta PIX
  cardDebitTax: 1.00,                           // Taxa da maquininha no débito (R$)
  cardCreditTax: 2.00,                          // Taxa da maquininha no crédito (R$)
  minOrder: 10.00,                              // Valor do pedido mínimo (R$)
  defaultDeliveryFee: 5.00,                     // Taxa de entrega padrão
  deliveryTimeMin: 45,                          // Tempo mín de entrega
  deliveryTimeMax: 70,                          // Tempo máx de entrega
};
```

Qualquer alteração feita nesse bloco atualiza automaticamente todos os cálculos, botões e mensagens do WhatsApp!

---

## 📱 Recursos Inclusos na Aplicação

- **Busca em Tempo Real**: Filtro instantâneo por nome ou ingrediente.
- **Abas de Categorias**: Navegação rápida com ícones e quantidade de itens.
- **Cardápio Completo Extraído do Yooga**:
  - Promoções 🔥
  - Sanduíches Tradicionais (X-Salada, X-Tudo, Artesanal, Supremo, etc.) 🍔
  - Kikão & Dogs (Tradicional, Com Queijo, Coalho, Bacon, etc.) 🌭
  - Batatas Fritas & Turbinadas 🍟
  - Combos Caixa (Combo Maluco, Brocado, Família, Larica, etc.) 📦
  - Pizzas Tradicionais, Especiais e Doces 🍕
  - Pastéis Fritos Recheados 🥟
  - Sucos Naturais e Refrigerantes 🥤
- **Modal de Personalização**: Campo para o cliente digitar observações (ex: "Sem cebola", "Ponto da carne").
- **Sacola de Compras Dinâmica**:
  - Escolha entre **Entrega** ou **Retirar no Balcão**.
  - Lista de 47 bairros com taxas calculadas automaticamente.
  - Formas de pagamento (PIX com botão copiar chave, Cartões com taxa, Dinheiro com troco).
- **Checkout Direto no WhatsApp**: Monta a mensagem completa e abre o WhatsApp da loja em 1 clique.
