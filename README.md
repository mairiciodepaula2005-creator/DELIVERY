# 🍔 Cardápio Digital & Delivery Web - Chapa Quente

Cardápio digital moderno, responsivo e interativo no formato de aplicativo de celular, inspirado fielmente na experiência do **Yooga Delivery** (`delivery.yooga.app/chapa-quente/tabs/home`).

---

## 🚀 Como Visualizar o Cardápio

Você pode abrir o cardápio de duas maneiras:

1. **Pelo Navegador (Servidor Local)**:
   - Acesse: **`http://localhost:8080/`**
2. **Direto pelo arquivo**:
   - Dê um duplo clique no arquivo **`index.html`** para abrir no Chrome, Edge ou qualquer navegador.

---

## 🎨 Como Inserir a sua Logo Oficial

O sistema já vem com uma logo provisória profissional vetorizada (`assets/img/logo-placeholder.svg`). Quando você estiver pronto para inserir a sua própria logo:

### Opção 1 (Mais fácil - Substituição de arquivo):
1. Salve a imagem da sua logo com o nome **`logo.png`** (ou `.jpg` / `.webp`) dentro da pasta **`assets/img/`**.
2. Abra o arquivo **`index.html`** no Bloco de Notas ou editor de código.
3. Procure por `assets/img/logo-placeholder.svg` (por volta da linha 48):
   ```html
   <img 
     id="store-logo" 
     class="store-logo-img" 
     src="assets/img/logo.png" 
     alt="Logo da Lanchonete" 
   />
   ```
4. Salve o arquivo e atualize a página no navegador.

### Opção 2 (Link / URL da internet):
Cole o link direto da imagem no `src`:
```html
<img id="store-logo" class="store-logo-img" src="https://seusite.com/sua-logo.png" alt="Logo" />
```

---

## ⚙️ Como Alterar WhatsApp, Chave PIX e Dados da Loja

Abra o arquivo **`js/products.js`**. Logo no início você encontrará as configurações:

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
  operatingHours: "Terça a Domingo das 18h às 02h"
};
```

---

## 📱 Recursos e Telas Inclusas

- **Formato 100% Mobile (App de Celular)**:
  - Centralizado no computador com proporções exatas de smartphone.
  - Ocupa 100% da tela em celulares reais, com suporte a entalhe de tela (*notch*).
  - Cards de produtos em 1 coluna vertical com fotos e botões rápidos.
- **Barra de Navegação Inferior (Estilo Yooga)**:
  - 🏠 **Início**: Retorna ao topo do cardápio.
  - 🧾 **Pedidos**: Histórico de pedidos realizados pelo cliente para repetir com facilidade.
  - 🎟️ **Cupons**: Cupons de desconto ativos com aplicação automática na sacola.
  - 👤 **Perfil**: Salva nome e WhatsApp do cliente no aparelho e botão de suporte.
- **Cardápio Completo Extraído do Yooga**:
  - 179 itens cadastrados em 13 categorias com fotos reais e descrições.
- **Sacola de Compras com Checkout via WhatsApp**:
  - Seletor de **Entrega (Delivery)** ou **Retirada no Balcão**.
  - 47 bairros com cálculo automático da taxa e tempo de entrega.
  - Opções de pagamento: **PIX** (com botão de copiar chave), **Cartão de Crédito/Débito** e **Dinheiro (com troco)**.
  - Finalização em 1 clique enviando o pedido formatado direto para o WhatsApp do restaurante.
