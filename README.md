
<strong>Introduction</strong>

A French Lemmatizer in Python based on the LEFFF (Lexique des Formes Fléchies du Français / Lexicon of French inflected forms) is a large-scale morphological and syntactic lexicon for French forked from https://github.com/ClaudeCoulombe/FrenchLefffLemmatizer and backported using 3to2 (https://pypi.python.org/pypi/3to2) to run on Python 2.X.

<strong>Main reference:</strong>

[Sagot,2010] Sagot, B. (2010). The Lefff, a freely available and large-coverage morphological and syntactic lexicon for French. In 7th international conference on Language Resources and Evaluation (LREC 2010). Retrieved from https://hal.archives-ouvertes.fr/file/index/docid/521242/filename/lrec10lefff.pdf

Benoît Sagot Webpage about LEFFF<br/>
http://alpage.inria.fr/~sagot/lefff-en.html<br/>

More precisely, we use the morphological lexicon only: .mlex file) which has a simple format in CSV (4 fields separated by '\ t')

<a href="https://gforge.inria.fr/frs/download.php/file/34601/lefff-3.4.mlex.tgz">LEFFF download hyperlink</a>

Tagset format FRMG - from the ALPAGE project since 2004<br/>
<a href="http://alpage.inria.fr/frmgwiki/content/tagset-frmg">Tagset</a>

<strong>License</strong>

Copyright (C) 2017-2018 Claude COULOMBE

Licensed under the Apache License, Version 2.0 (the 'License');
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

<a href="http://www.apache.org/licenses/LICENSE-2.0">Apache 2.0 License</a>

-----

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an 'AS IS' BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Installation:

1) Download the .zip file and uncompress it
2) Rename the file FrenchLemmatizer-master to FrenchLemmatizer
3) Using the console:<br/>
`> cd FrenchLemmatizer`<br/>
4) You should install pip (https://packaging.python.org/tutorials/installing-packages/)<br/>
`> pip install . `

-----

Small examples:

``` Python
from FrenchLefffLemmatizer.FrenchLefffLemmatizer import FrenchLefffLemmatizer
french_lemmatizer = FrenchLefffLemmatizer()
print(french_lemmatizer.lemmatize('avions'))
avion
french_lemmatizer.lemmatize('avions','n')
avion
french_lemmatizer.lemmatize('avions','v')
avoir
french_lemmatizer.lemmatize('avions','all')
[('avion', 'nc'), ('avoir', 'auxAvoir'), ('avoir', 'ver')]
french_lemmatizer.lemmatize('vous','all')
[('se', 'clr'), ('le', 'cla'), ('lui', 'pro'), ('il', 'cln'), ('lui', 'cld')]
french_lemmatizer.lemmatize('la','all')
[('la', 'nc'), ('le', 'det'), ('le', 'cla')]
```



