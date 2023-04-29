# Occam-IDE

Occam's IDE.

### Contents

- [Road map](#road-map)
- [License](#license)
- [Contact](#contact)

## Road map

This road map summarises the remaining features considered necessary for Occam to become a usable system. It covers not just the IDE but also the verifier and the Open Mathematics website.

1 **Indexing** This needs to be improved in order to support labels and references with terms. Some of the recent work on the verifier, in particular substitution, could be leveraged.

2 **Verification** A more or less complete verifier should verify not just at the meta level. An acid test would be verifying induction, both the proof of its rule and its application to, say, a proof that all natural numbers are either even on odd.

3 **Left recursionr** The current algorithm is ill-conceived. A new algorithm will be based on a graph-theoretic approach. The corresonding paper will then require an almost complete rewrite.

4 **Directed graphs** Devise an algorithm based on the Pearce-Kelly algorithm that supports cycles. The current implementation tacks cyclic edges onto the side of the aforementioned algorithm, and is surprisingly complicated. Better to extend the existing algorithm and write a short paper. Also, test the other graph algorithms. 

There is no particular order and some items, for example editing, can be considered as desirable rather than strictly necessary. The last item can be expended considerably but perhaps a first goal would be to just get verification working in memory, so to speak.

## License

Copyright 2016-2023 James Smith

Licensed under the Apache License, Version 2.0 and Anti-996 License (collectively the "License"); you may not use this software except in compliance with the License and subject to the terms laid out after this notice. A copy of the License can be found at the following URL:

  https://github.com/djalbat/occam/blob/master/license.txt

Unless required by applicable law or agreed to in writing, software distributed under the Licenses is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the Licenses for the specific language governing permissions and limitations under the Licenses.

### Terms

* This is **not** free software.
* It can be used *only for personal use and if not for profit*, otherwise you must contact the author.
* You cannot re-use the source code for any reason, even if only for personal use and if not for profit; or even if you have paid to use it otherwise.

## Contact

* james.smith@openmathematics.org
