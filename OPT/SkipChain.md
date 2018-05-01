Cothority that manages the SkipChain : $C_v$, creates for each server a private key and sign. Do they insert in chain $SkC$

- Yes, Genesis block = signatures and pub key, if update, need to change, how ? New Skipchain ?
- No, will need to exchange each time with DP.

DP computes the value for its value $\sigma$, send to the $C_v$ a structure containing all information needed to Verifiy, called $proof_{\sigma}$.

The $C_v$ insert $proof_{\sigma}$ into $SkC$

Then 2 choice : 

- Verify all, insert a Merkle Tree of proof inside a block
  - ++ To verify proof, you just take the merkle and check it.
  - -- Takes time to verify, if false block for nothing.
- Do not Verify, let the work be done by someone else
  - ++ Fast and cheap
  - -- You can insert wrong stuff in the chain, but also non desirable stuff
  - -- Can be spammed to insert stuff in $SkC$ ? (Can you really)

