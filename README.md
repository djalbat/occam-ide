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

2. **Sessions** Broken since moving the concurrency server to a lambda, this can be fixed by using Redis rather than storing shared documents in memory. The session pane will also need to be altered along much the same lines as the projects pane. There are also bugs relating to leaving sessions and selection timeouts that need to be fixed.

3. **Verification** Halfway to completiion, with verification when publishing already done. A more or less complete verifier needs to verify not just at meta level. There also needs to be some improvement in the indexing. An acid test would be verifying induction, both the proof of its rule and its application.

4. **Projects pane** Add functionality to rename existing files and directories as well as add new ones. This requires entries in the explorer to be selectable as well as a redesign of the projects pane to include a bar with the requisite icons.

5. **Directed graphs** Devise an algorithm based on the Pearce-Kelly algorithm that supports cycles. The current implementation tacks cyclic edges onto the side of the aforementioned algorithm, and is surprisingly complicated. Better to extend the existing algorithm and write a short paper. Also, test the other graph algorithms. 

6. **Worker threads for custom grammars** Currently combined custom grammars are re-calculated whenever non-trivial changes are made to BNF or lexical pattern files. Whilst the custom grammars functionality is gratifyingly fast, re-calculating on nearly every key press nonetheless interferes a little with the user experience. So these calculations can be carried out in a worker thread. This could also pave the way for verification to be integrated with the IDE.

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
