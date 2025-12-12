# Dado o diálogo acima, você deve conseguir responder as seguintes perguntas:

[x] Quais as entidades de domínio?

[] Quais as ações (casos de uso) que essa aplicação deve ter?

## Requisitos Funcionais 

1. Gerenciamento de estoque
2. Tracker Individual
   - Id
   - Informaçoes extra:
     - Tamanho
     - Cor
3. Definir Quantidades minimas de estoque
   - Número variável para cada tipo de produto
4. Alertas quando chegar a um determinado número de items no estoque
   - Alertas por email
   - Sistema de notificação próprio
5. Histórico de vendas
   - Data
   - Quantos produtos venderam em um periodo
   - Lucro gerado
   - Qual produto está vendendo melhor
   - Tendencias
  
## Requisitos não funcionais

1. Criar e gerenciar ordens de compra automaticamente
   - Base quantidade minima de destoque
   - Tendencias
2. Intregração de sistemas entre fornecedores
   - Atualizaçoes automáticas sobre prazos

### Entidades

- Product
- Tracker
- Sell
- Notification
- NotificationByEmail
- NotificationBySystem
- Vendor
- Stock
- BuyOrder


### Use Cases

#### Product
- RegisterProductUseCase
- UpdateProductUseCase
- DeleteProductUseCase
- FindProductUseCase
- ListProductsUseCase

#### Sell
- RegisterSellUseCase
- UpdateSellUseCase
- CancellSellUseCase
- RevertSellUseCase
- CalculateProfitUseCase
- VisualizeSellTrendsUseCase
- VisualizeBestSellersByDate

#### Track
- RegisterTrackerUseCase
- ListTrackers
- UpdateTracker
- TrackProductByIdUseCase
- TrackProductByColorUseCase
- TrackProductBySizeUseCase
- TrackProductByAttributesUseCase
- TrackProductLocationUseCase
- VisualizeHistoryTracker

#### Stock
- DefineMinimalQuantityInStockUseCase
- UpdateStockUseCase
- FindStockUseCase
- ListStockUseCase
- VerifyStock
- VisualizeHistoryStockUseCase
- OnLowSotckNotify

#### Notifcation
- SendNotificationByEmailUseCase
- SendNotificationBySystemUseCase
- ListNotificationsUseCase
- MarkNotificationAsReadUseCase

#### Vendor
- RegisterVendorUseCase
- UpdateVendorUseCase
- DeleteVendorUseCase
- FindVendorUseCase
- ListVendorsUseCase
