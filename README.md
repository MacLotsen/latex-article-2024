# NTG Article

This project contains the following components:

the-introduction
:   An introduction by the author (Erik Nijenhuis).

the-article
:   The article featuring a demo on `lua-placeholders` and GinVoice.

invoice-template
:   An example from the demo folder.

invoice-001
:   An example from Grapefruit Inc. in the demo folder.

invoice-002
:   An example from Xerdi in the demo folder.

invoice2-template
:   An example from Grapefruit Inc. in the demo-splitted folder.

There are more examples that can be generated, however, they are not used as attachments in the article.

## Output
To compile the examples, you need `lua-placeholders` version 1.0.2.
This version is currently unreleased and can only be obtained via [GitHub](https://github.com/Xerdi/lua-placeholders) in the meantime.
Furthermore, there are 3 Makefiles:
 - src/Makefile
 - src/demo/Makefile
 - src/demo-splitted/grapefruit/Makefile

To compile the components, these Makefiles have been configured for Windows 10 and Ubuntu with a recent TeX Live distribution (not from apt).

To compile all standard components, you can execute `make all` in the `src/` directory.
