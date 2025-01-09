# EPI Proof-of-Concept Code - Policies
This code contains example policy for the Brane framework that can be used for the proof-of-concept described in [\[1\]](../README.md#references). Concretely, it limits what individual domains are willing to execute within Brane.


## Structure
There are three files that represent the implemented policy for the three domains: [`st_antonius.eflint`](st_antonius.eflint) implements the policy for the St. Antonius; [`umc_utrecht.eflint`](./umc_utrecht.eflint) implements the policy for the UMC Utrecht; and [`surf.eflint`](./surf.eflint) implements the policy for the trusted third-party domain SURF.

In Brane itself, all of these three policies live on different machines and are completely separate. However, for simplicity's purpose, all three depent on the fourth file, [`model.eflint`](./model.eflint), which describes the shared concepts that need be explained to eFLINT. Things like this are what a task is, what a dataset is, etc.

Finally, the [`examples/`](./examples/)-folder contains a few more eFLINT files that give examples for scenarios that Brane would generate to check policy compliance. Specifically, at runtime, Brane would compile a file akin to e.g. [`examples/scenario1_ok.eflint`](./examples/scenario1_ok.eflint), which, once run by the reasoner, would either trigger a violation or not. In the latter case, that domain's worker would happily execute the presented workflow; whereas in the first, it would not execute anything. As such, it is useful to think of the scenario files as hypothetical scenarios of which we want to check compliance. If it the hypothetical scenario does not violate anything, it is executed; otherwise, we don't do it.


## Usage
You can run these eFLINT files using the [Haskell implementation](https://gitlab.com/eflint/haskell-implementation) of the eFLINT interpreter. The main page shows a how-to for installing the reasoner.

Then, you can run a scenario by running e.g.:
```sh
eflint-repl ./policies/examples/scenario1_ok.eflint
```
in a terminal and observe whether violations occur.
