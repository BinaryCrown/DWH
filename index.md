A website to try to find preimages of the deep web hash (DWH) <code>36367763ab73783c7af284446c59466b4cd653239a311cb7116d4618dee09a8425893dc7500b464fdaf1672d7bef5e891c6e2274568926a49fb4f45132c2a8b4</code>. This is a monstrous task - all the work is done on the client side, so if enough people use the website the work might be distributed enough to find hits.

The deep web hash was revealed by the mysterious group Cicada 3301 -- for all we know, they could be a cult or intelligence agency -- in the "Liber Primus" (lit. first book), a pseudoreligious text which centers heavily on similar topics to Hofstadter's "Goedel, Escher, Bach", namely Zen, kōans, number theory, truth and meaning, as well as other topics such as privacy (much of it has still not been translated and deciphered). The excerpt of interest is from page 56:

> **An End**
>
> Within the Deep Web there exists a page that hashes to <code>36367763ab73783c7af284446c59466b4cd653239a311cb7116d4618dee09a8425893dc7500b464fdaf1672d7bef5e891c6e2274568926a49fb4f45132c2a8b4</code>.
>
> It is the duty of every Pilgrim to seek out this Page.

It is strongly believed that this is a legitimate challenge. So far, such a page has not been found, in any of the interpretations of "hashes to": it is unclear whether we should contain the hash of the whole source code, or just the visible text, or the code of a single e.g. image on the webpage, and it is unclear which hash algorithm is to be used.

This project is, as written above, an attempt to find any strings which hash to this, by distributing the work over many devices. Inverting hashes is difficult and, for modern hash algorithms such as SHA-2 (specifically, SHA-1024) no method significantly better than bruteforce is known.
