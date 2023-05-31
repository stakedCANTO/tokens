# BLOTR Protocol Tokens

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can
be used by any dApp interfaces that needs one or more lists of tokens. Anyone can create and
maintain a token list, as long as they follow the specification. The BLOTR community invites
you to add your favorite tokens to our tokenlists!

## Adding Your Token to an Existing List

### General Requirements
1. Token should be verified on [Sourcify](https://sourcify.dev/#/verifier).
2. Token must be added to a list that it qualifies for:
    * **[BLOTR Protocol Tokenlist](./blotr.tokenlist.json)**: Token must be part of BLOTR Protocol.

## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Please use the [checksum address](https://docs.ethers.io/v5/api/utils/address/#address). Here is an example using PNG:
    ```json
    {
      "chainId": 7700,
      "address": "0xFf0BAF077e8035A3dA0dD2abeCECFbd98d8E63bE",
      "decimals": 18,
      "name": "BLOTR Protocol",
      "symbol": "BLOTR",
      "logoURI": "https://raw.githubusercontent.com/stakedCANTO/tokenlists/master/logos/blotr.jpg"
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name,
    symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and
    should be a major version update.

## Adding Your Token Logo

Token logos are [hosted here](https://github.com/stakedCANTO/tokens/logos).
