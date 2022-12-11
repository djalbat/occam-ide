# Occam

A formal, automated domain of reasoning.

### Contents

- [Road map](#road-map)
- [Licenses](#licenses)
- [Terms](#terms)
- [Contact](#contact)

## Road map

This road map summarises the features, and fixes, considered necessary for Occam to become a usable system, in terms of both the software and the theory behind it. It covers not just the IDE but also the verifier and the Open Mathematics website.

1. **Editing** Add support for multiple cursors, folding, multiline indentation and streamlined comments. This entails, amongst other things, overriding the default undo and redo functionality. The is also the possibility to improve the user experience for larger documents by incremental rendering. Finally, there still remains a problem with deferred events.

2. **Sessions** Broken since moving the concurrency server to a lambda, this can be fixed by using Redis rather than storing shared documents in memory. There are also bugs relating to leaving sessions and selection timeouts that need to be fixed. Hopefully Redis' logging functionality, whatever it turns out to be, with help with this.

3. **Verification** Halfway to completiion, with verification when publishing already done. A more or less complete verifier should verify not just at the meta level. An acid test would be verifying induction, both the proof of its rule and its application to, say, a proof that all natural numbers are either even on odd. 

4. **Indexing** This needs to be improved in order to support labels and references with terms. Some of the recent work with the verifier, in particular substitution, can be leveraged here. A likely side effect of this work will be the ditching of overlay tokens, which will simplify things considerably. This work will be related to the rendering changes as well.

5. **Directed graphs** Devise an algorithm based on the Pearce-Kelly algorithm that supports cycles. The current implementation tacks cyclic edges onto the side of the aforementioned algorithm, and is surprisingly complicated. Better to extend the existing algorithm and write a short paper. Also, test the other graph algorithms. 

6. **Rewrite the left recursion elimination paper** Hardly a necessity. However, the current paper is now woefully out of date and, besides, the exercise will afford the chance for one last critical evaluation of the algorithm. Whilst there are no certainties, the algorithm is too complex for a correctness proof, for example, nonetheless it would be good to at least try to put this one to bed.

There is no particular order and some items, for example editing, can be considered as desirable rather than strictly necessary. The last item can be expended considerably but perhaps a first goal would be to just get verification working in memory, so to speak.

## Licenses

Copyright 2016-2019 James Smith

Licensed under the Apache License, Version 2.0 and Anti-996 License (the "Licenses"); you may not use this software except in compliance with the Licenses and subject to the terms laid out after this notice. A copy of the Apache License can be found at the following URL:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the Licenses is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the Licenses for the specific language governing permissions and limitations under the Licenses.

## Terms

* Occam can be used *only for individual use and if not for profit*, otherwise you must contact the author.
* The majority of the projects of which Occam is comprised are open source, but Occam itself is not.
* You cannot re-use the source code for any reason unless directly from the aforementioned open source projects.

## Contact

* james.smith@openmathematics.org
