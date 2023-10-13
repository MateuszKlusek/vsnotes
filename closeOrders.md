v1StrategyClosePost from api.ts to close order (confirm)

close order 
- close order itself (it removes liquidity on its own, no extra step required)
- remove from db

UserOrderHistory - useOrderHistory hook

OrderHistoryRow - there's a modal planted

we get strategyId (entry.strat_id) so be map to our db as `externalId`

mockOrdersPayloads - mocks



prisma.StrategyMetaData -> algorithmVersionId matched to 
prisma.algorithmVersion -> id


prisma.algorithmVersion (algorithmId) =  prisma.algorithm (id)

błędy pojawiają się w momencie transformacji danych z naszej db (algorithm i algorithmVersion) przy pobieraniu danych w CH


---- CR fixes

StrategyCopyContainer - there's a signTransaction and submitOrder (check it)


flow:
- closeOrder (rename to stopOrder)
- signTransaction in the browser
- submitStopOrder - new mutation that works similarly to current submitOrder, but changes the status to CLOSED.




# connect with the gateway

stopHandle -> 


stopOrder (mutation) -> buildStopOrderTransaction (got txCbor) -> 


handler 
addLiquidity (mutation) -> addLiquidityToOwnStrategy 
buildAddLiquidityToStrategyTransaction (order.txCbor)



