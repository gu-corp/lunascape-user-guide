---
navigation:
  order: 200
---

# Sending and transaction problems

## "Fees (gas) are insufficient." appears

Fees are paid in the network's own currency, separately from the token you send (ETH on Ethereum, JOC on Japan Open Chain). Receive a little of that currency, or [buy it on an exchange](../features/assets.md#trade-a-token), then try again. See [Send](../features/send.md).

## "Cannot estimate gas" appears

Something is wrong with the transaction, or the network is too busy to estimate the fee.

- Check your balance, the amount and the recipient.
- Wait a while and try again.
- A screen may let you enter a gas value and continue, but don't continue if you don't know what value to use.

## A send won't finish (stays pending)

When the network is busy, transactions with low fees are processed later.

- Waiting a while often lets it finish.
- Open the pending transaction from **Transaction History** to raise its fee and speed it up, or to cancel it. Canceling also costs a fee, and other pending transactions may be canceled too.
- Switching networks while a transaction is pending cancels all pending transactions.

## "Nonce is too low." appears

The transaction's number (nonce) clashes with an earlier one from the same account. Check **Transaction History** for pending transactions, and send again once they finish.

## Received, but the balance doesn't appear

1. Check that the network the sender used matches the network shown for the token in your asset list (USDT on Ethereum and USDT on Japan Open Chain are different tokens).
2. Press the refresh icon on the main screen.
3. If the token isn't in your list, [add the token](../features/assets.md#add-a-token).
4. Ask the sender for the transaction ID (transaction hash) and check in a block explorer that it completed.

## "Can't connect to the network" appears

- Check your internet connection.
- For a network you added yourself, check that the Network URL (RPC URL) is right.
- Wait a while and try again.

## Reversing or refunding a transaction

No one can reverse a transaction recorded on the blockchain. Lunascape can't refund or recover it either.
