---
navigation:
  order: 700
---

# Connect to sites

Open a Web3 site (DApp) in Lunascape Browser. When the site asks the wallet for something, a confirmation screen appears. Read it before you allow anything.

> **Important:** Connecting tells the site your address. A signature may give the site permissions, and a transaction moves assets and can't be reversed. Only approve requests from sites you trust, and never enter your seed phrase or private key on a website.

## Connect to a site

1. On the site, tap its connect button (such as **Connect Wallet**). If the site lists wallets, choose Lunascape, or MetaMask if Lunascape isn't listed.

   <img src="img/mobile-connect-site.png" alt="The ChainList site in Lunascape Browser with a Connect Wallet button" width="300" />

2. The wallet shows **The site is requesting your wallet address**. Check the site's name and URL and the account, then tap **Approve**. Tap **Cancel** to refuse.

   <img src="img/mobile-connect-request.png" alt="The Connect screen: The site is requesting your wallet address, with the site ChainList and its URL, Account 1 (address blurred), and Cancel and Approve buttons" width="300" />

3. You return to the site, which now shows that it's connected. How it shows this depends on the site.

   <img src="img/mobile-connect-after.png" alt="ChainList after connecting, with the address shown at the top" width="300" />

Connecting alone never sends any crypto.

## See or remove connected sites

In the wallet's settings, **Permitted websites** lists the sites you've allowed, by account.

<img src="img/mobile-settings-permitted.png" alt="Permitted websites listing two sites under Account 1, and an Add to List button" width="300" />

To disconnect a site, tap it, then tap **Delete Site** and **Delete**.

<img src="img/mobile-settings-permitted-detail.png" alt="Website detail with the Site URL and a Delete Site button" width="300" />

<img src="img/mobile-settings-permitted-delete.png" alt="Delete permitted site: Are you sure you want to delete this site? with Cancel and Delete" width="300" />

**Add to List** lets you allow a site in advance by entering its URL.

<img src="img/mobile-settings-permitted-add.png" alt="Add permitted website with a Site URL field and an Add to List button" width="300" />

## Requests a site can send

### Signature request

The site asks you to sign a message, for example to prove you own the address. Signing doesn't send any crypto, but some signatures give a site permission to use your tokens. Tap **Sign** only if you understand the message and trust the site.

<img src="img/mobile-sign-personal.png" alt="Signature Request with an example message, Account 1 (address blurred), and Cancel and Sign buttons" width="300" />

<img src="img/mobile-sign-typed.png" alt="Signature Request showing structured data (contents, from, to and wallets), and Cancel and Sign buttons" width="300" />

### Transaction approval

The site asks you to send a transaction (a payment, a swap and so on). Check the **Amount of payment**, the **Transaction Fee** and the site under **Client**, then tap **Approve**. If your balance isn't enough, **Insufficient balance** appears and you can't approve.

<img src="img/mobile-tx-approval.png" alt="Transaction Approval with Amount of payment, Transaction Fee, Client (the site), Insufficient balance, and Cancel and a disabled Approve button" width="300" />

### Add tokens

The site suggests tokens to add to your asset list. Adding only shows them in the list. Tap **Add tokens** if the token is the one you expect.

<img src="img/mobile-dapp-add-token.png" alt="Add Suggested Tokens: Would you like to add these tokens? with DAI and its balance, and Cancel and Add tokens buttons" width="300" />

### Add or switch a network

The site asks to add a network to the wallet, or to switch to one. Check the chain name, chain ID and RPC URL, then tap **Approve**.

<img src="img/mobile-dapp-add-network.png" alt="Add Network: Allow this site to add a network? with Chain Name, Chain ID, RPC URL and Currency Symbol, and Cancel and Approve buttons" width="300" />

<img src="img/mobile-dapp-switch-network.png" alt="Switch network: Allow this site to switch the network? with Base, and Cancel and Approve buttons" width="300" />

> **Note:** These two screens still show the wallet's former name, G.U. Wallet. It's the same wallet.

## MetaMask compatibility

Some sites only work with MetaMask. Turn on **Enable ethereum.isMetaMask** in the wallet's settings, reload the page, and choose MetaMask on the site. See [Settings](settings.md).
