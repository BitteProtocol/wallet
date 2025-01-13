
# @bitte-ai/wallet


This is the [Bitte Wallet](https://wallet.bitte.ai) SDK package.
You can check a quick example of Simple Login using Next.js 14 and @bitte-ai/react

check our [React integration](https://docs.mintbase.xyz/dev/mintbase-sdk-ref/react#mintbasewalletcontextprovider)

Example:
You can check a [quick example of Simple Login](https://github.com/Mintbase/examples/tree/main/starter) using Next.js 14 and @mintbase-js/react


<p align="center">
<img  src='https://img.shields.io/npm/dw/@mintbase-js/wallet'  />
<img  src='https://img.shields.io/bundlephobia/min/@mintbase-js/wallet'>
</p>

## Video tutorial

https://github.com/Mintbase/mintbase-js/assets/8454267/7301c178-3a34-497c-a2e7-1616d8f8b6a2





## Installation and Usage



The easiest way to use this package is to install it from the NPM registry, this package requires `near-api-js` v1.0.0 or above:



```bash

# Using Yarn

yarn  add  near-api-js


# Using NPM.

npm  install  near-api-js



# Using PNPM.


pnpm  install  near-api-js



```



```bash

# Using Yarn

yarn  add  @bitte-ai/wallet



# Using NPM.

npm  install   @bitte-ai/wallet



# Using PNPM.

pnpm  install   @bitte-ai/wallet



```



Then use it in your dApp:




{% code title="setup.ts" overflow="wrap" lineNumbers="true" %}




```ts
import { setupWalletSelector } from  "@near-wallet-selector/core";
import { setupBitteWallet } from  " @bitte-ai/wallet";

const  wallet = setupBitteWallet({
    networkId:  'mainnet',
    walletUrl:  'https://wallet.bitte.ai',
    callbackUrl:  'https://www.mywebsite.com',
    deprecated:  false,
});

const  selector = await  setupWalletSelector({
    network:  "mainnet",
    modules: [wallet],
});
```

{% endcode %}




## setupBitteWallet



- `networkId:` Near Networks
- `walletUrl:` valid wallet urls
- `successUrl:` If you dont have a single callback entrypoint to handle failure/success you can set successUrl.
- `failureUrl:` If you dont have a single callback entrypoint to handle failure/success you can set failureUrl.
- `callbackUrl:` when you have a single entrypoint to deal with transaction results.
- `contractId`: the ContractId that your dapp will be using aka (receiverId)

## Troubleshooting

**Client-side only:**
The wallet runs only on client-side.

Any other questions or issues you can contact support on our [Telegram Channel](https://telegram.me/mintdev).

## License

This repository is distributed under the terms of both the MIT license and the Apache License (Version 2.0).
