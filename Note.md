`signal.MarketStats` 



problem occurred with add funds and withdraw funds
 data: 'Could not find Strategy policy with id EncodedText Base16 "0ddf4cb6cdf1579f7e32bc4a270aae0d2860a9a2f796e8e2076fbf45"'

adding gas
data: 'Error in $.nodeAllocation[0].assets[0].quantity: parsing Natural failed, expected Number, but encountered Null'

after 
fix the Number(amount) - handleSubmit in  `app/strategies/components/FundStrategyModal/index.tsx`
fix types in `app/strategies/validation.ts`

we have the "Could not find Strategy policy with id error, not for everything
- add asset
- add gas
- remove asset
- remove gas(double check?????)


what if we remove all asset?

----

limit algo externalId - `3d525f720592d17bcd05d08ed182e5edd313b8e6d4ac0686dc642a39`



 Memory limit (total) exceeded: would use 5.69 GiB (attempt to allocate chunk of 8388608 bytes), maximum: 5.40 GiB. OvercommitTracker decision: Memory overcommit has freed not enough memory. 