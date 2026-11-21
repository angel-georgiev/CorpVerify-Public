# CorpVerify

**Try the demo:** <https://angel-georgiev.github.io/CorpVerify-Public/>

## What CorpVerify is

In corporate due diligence (for example, know-your-customer and anti-money-laundering checks), one organisation often sends a package of evidence about a company to another: registry extracts, ownership records, identity documents. Later it is hard to prove that the package someone reviewed is exactly the one that was sent, or to reconstruct who submitted, received, reviewed or replaced which version and when.

CorpVerify is a proposed **permissioned blockchain** shared by a consortium of organisations such as banks, corporate service providers and law firms. It records:

- the **hash** (digital fingerprint) of each evidence package, so anyone holding the documents can check they are unchanged;
- the **workflow events** around it: *submitted*, *receipt acknowledged*, *review completed*, *correction requested*, *superseded*;
- **who** did each step: which organisation, and which authorised employee account.

The documents themselves never go on the blockchain. They stay in each organisation's own secure storage and are shared through existing channels.

CorpVerify does **not** judge whether evidence is true, approve a company or make a compliance decision. Human review stays necessary.

## The demo

The demo runs entirely in your browser. It simulates the CorpVerify ledger and its rules inside the page: nothing is uploaded, and reloading the page resets it. Use the **Acting as** menu to switch between participants, and the **How it works** tab for a guided walkthrough.

A short tour:

1. As **Alice** (submitter at Atlas Corporate Services), choose *Use sample documents* and *Submit to CorpVerify*. Only the package's hash is recorded.
2. As **Bob** (reviewer at Northbridge Bank), tick *simulate a document altered in transit*, load the files and try to *Acknowledge receipt*. The ledger refuses, because the hash no longer matches.
3. Untick it, load the files again, acknowledge receipt and *Request correction*.
4. As **Alice**, prepare a corrected version and submit it. Version 1 is marked **Superseded** but kept in the history.
5. As **Bob**, acknowledge and *Record review completed*.
6. In **Verify a package**, load either version and look it up to see its record and full version history.
7. In **Ledger**, tamper with a sealed block and verify the chain to see the broken link.

## Status

CorpVerify is a student team project. This demo is a proof of concept, not a production system.

## License

[MIT](LICENSE)
