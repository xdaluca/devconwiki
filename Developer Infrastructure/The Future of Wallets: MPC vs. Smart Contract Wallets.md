# The Future of Wallets: MPC vs. Smart Contract Wallets

* Status: Edited ✔️
* Speaker: Ivo Georgiev
* Date: Day 4 - Oct 14, 2022
* Skill level: Intermediate
* Track: Developer Infrastructure
* Keywords: mpc,multi-party computation,ux,smart wallets
* Video link: https://youtu.be/85w0TvZMivA
* Slides link: to be provided by speaker
* Description: <br>
_There's undoubtedly more we can do to improve Ethereum wallet UX, and there's two technologies competing for this: MPC (multi-party computation) and smart contract wallets.
Let's explore the relative strenghts and weaknesses of each, as well as the protocol upgrades that will help (eg account abstractions, EIP3074 and EIP4337) and how those affect the comparsion._
<br>

# Notes

**Question**: Can be the future for the next 1 Billion crypto users?<br> 
**Myth**: Most people are not ready for self-custody<br>
**Reality**: Most self-custodial wallets are not ready for users<br>
<br>

Curent self-custody issues:<br>
* seed pahrases, back-up techniques
* compromised keys/software wallets vulnerable to malware & supply chain attacks
* social engineering attacks (eg BAYC)<br>
<br>

How do we prevent this? —> multi-factor authentication, aka **multisigs**<br>
<br>

Why are multisigs (kind of) a silver bullet?<br>
* seedless onboarding: you’re onboarded with 2 devices/separate time-locked recovery key
* account recovery (eg social recovery)
* multi-factor authentication
* resistance to hacks or compromised keys<br>
<br>
<br>

**MPC vs. smart contract wallets/account abstractions — which tech is the future?**
* MPC = multi-party computation -> In MPC wallets the signatures must be produced by 2 or more separate parties => this is _a_ multisig<br>
* SCW = smart contract wallet -> In smart wallets each user account is a *smart contract*, allowing for any custom authentication or execution logic => this wallet _inlcudes_ multisig features. <br>
<br>
<br>

**Smart contract wallet mythbusting**<br>
<br>
Myth: smart wallets can’t sign messages<br>
Reality: smart wallets can sign messages via EIP 1271<br>

Myth: smart wallets produce a different address on each chain, and require setup<br>
Reality: thanks to CREATE2, smart wallets can be counterfactually deployed on any EVM chain<br>

Myth: smart wallets have huge gas overhead<br>
Reality: thanks to minimal proxies, the permanent gas overhead is ~3k gas (delegatecall)<br>
<br>
<br>

**The case for smart wallets**<br>
* More than multisigs: timelocks/spending limits/recovery mechanisms(eg Argent social recovery)/ safe seedless onboarding and recovery (eg Ambire email/pass authentication)
* Mutable: change authentication scheme, rotate keys, add/remove signers (without changing address!)
* Gas abstractions: paying transaction fees in ERC20 tokens
* Batching: grouping multiple operations in one transaction => safely hiding ERC20 approvals (+ saves 21k gas base!)
* Automations: Instadapp, DeFi Saver - eg auto-harvesting rewards
* Flash loans: Furucombo
* Alternative cryptography: NIST curve (Ed25519), paving the way to using WebAuthn, iOS biometrics<br>
<br>
<br>

Drawbacks & adoption challenges for smarr contract wallets<br>
* Gas overhead: 30-40k gas on first transaction, 2k gas afterwards
* EIP 1271 largely unadopted, especially on front-ends
* Developer education!: (some) devs intentionally block smart contracts, not realizing contracts can be wallets /“bot protection”<br>
<br>
<br>

**MPC wallets distinct advantages**<br>
* Off-chain recovery —>  cheaper & easier, not as flexible as SCW
* Truly cross-chain, no dependence on smart contracts —> Bitcoin support!
* No gas overhead
* No need for any changes in dApps (signatures just work)<br>
<br>
<br>

Problems with MPC wallets<br>
* Custom cryptography required -> not ideal security-wise
* Immutable authentication rules—> no timelocks, limited to multisig (TSS)
* No current Trezor/Ledger compatibility<br>
<br>
<br>

**Conclusion**
* Smart contract wallets/account abstractions are more flexible and future proof
* MPC can be a fantastic transitory solution for specific use cases<br>
<br>
<br>

Contact:<br>
Ivo Georgiev, CEO Ambire Wallet<br>
ivo@ambire.com<br>
Twitter:@Ivshti



