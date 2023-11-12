https://www.figma.com/file/7kMARrNYP5HObNfCYNl6Kk/Design-Library---Trading-Platform?type=design&node-id=6321-59597&mode=dev

- `userId`?
- `walletAddress`?
- `priority`? (coming from GL or inferred from JSON body status, if we can organize it well) (can default on FE)
- `notificationType`: "text" | "credit"
- `createdAt`
- `notificationBody` - loose JSON, but we would need to have values like: 
    - `strategyId`? (necessary for adding liquidity, credits only)
    - `creditsLeft`? in strategy
    - `creditsUsed`?
    imagining a scenario -> started with credit of 5, to a refilling point used 4.75 / left with 0.25 (two two values: used and left are being shown in the notification item), added 4 credits, so we have 4.75 used / 4.25 left and notification notification status might be `watch` or `low` (depending on the ratio)
    - `status`? that would indicate that action (eg. `copied` for strategy got copied) (unless we forgo it and wait for the headerText)
    - `headerText`: since we have multiple variants (ADA/AXO, CardanoTop 10, Swapped ADA for MELD, etc), would be hard to catch all the versions
    - `itemType`: like "Strategies" or "Market order" for navigation purposes



We basically have two types of notification items - credit and text 
- with gas we have two versions of it - one is in Notifications tab (with no colored gauge) and second one in Credit alerts tab (with gauge)
- text

Questions
- we have two tabs `Notifications` and `Credit alerts` - do we show in `Notifications` all notifications and in `Credit alerts` only credit-related, all do we separate all notifications into general and credit alerts, with no overlapping. Since we have two UI versions for credit notification items (one for notifications and one for credit alerts), the former makes sense. Wanna confirm it. 
- `credit alerts` - we have different statuses, from figma there is "empty" | "very low" | "low" | "watch" - I assume that's the FE only metric and it's based on the percentage of credit used to starting amount of credit


