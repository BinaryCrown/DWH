A website to try to find preimages of the deep web hash (DWH) <code>36367763ab73783c7af284446c59466b4cd653239a311cb7116d4618dee09a8425893dc7500b464fdaf1672d7bef5e891c6e2274568926a49fb4f45132c2a8b4</code>. This is a monstrous task - all the work is done on the client side, so if enough people use the website the work might be distributed enough to find hits.

The deep web hash was revealed by the mysterious group Cicada 3301 -- for all we know, they could be a cult or intelligence agency -- in the "Liber Primus" (lit. first book), a pseudoreligious text which centers heavily on similar topics to Hofstadter's "Goedel, Escher, Bach", namely Zen, kōans, number theory, truth and meaning, as well as other topics such as privacy (much of it has still not been translated and deciphered). The excerpt of interest is from page 56:

> **An End**
>
> Within the Deep Web there exists a page that hashes to <code>36367763ab73783c7af284446c59466b4cd653239a311cb7116d4618dee09a8425893dc7500b464fdaf1672d7bef5e891c6e2274568926a49fb4f45132c2a8b4</code>.
>
> It is the duty of every Pilgrim to seek out this Page.

It is strongly believed that this is a legitimate challenge. So far, such a page has not been found, in any of the interpretations of "hashes to": it is unclear whether we should contain the hash of the whole source code, or just the visible text, or the code of a single e.g. image on the webpage, and it is unclear which hash algorithm is to be used.

This project is, as written above, an attempt to find any strings which hash to this, by distributing the work over many devices. Inverting hashes is difficult and, for modern hash algorithms such as SHA-2 (specifically, SHA-512) no method significantly better than bruteforce is known.

# Time complexity

On an average consumer-grade single-core PC, one can perform 2.4 billion operations per second. The SHA-2 algorithm has a linear, i.e. O(n), time complexity, so (assuming a t.c. constant of at most 60, which is generous) we can hash 40 million bytes a second. In a 512-bit hash algorithm (like the one used for the DWH) there are approximately 10^148 million possible hashes, so brute-forcing all hashes on an average consumer-grade single-core PC would take at most 4 x 10^147 days - still nowhere close to imaginable (this estimate is likely inaccurate as hashing longer strings requires more time, so we can hash lots of short strings initially and then we'll slow down, rather than hashing a single 40 million byte string every second). The search for the DWH is somewhat facilitated by the following factors (in order of descending importance):

- We obviously don't have to check *every* hash to find just the DWH. The DWH may be the hash of a relatively short string compared to preimages of other hashes; this is quite likely as, if the "hash" of a webpage means the hash of its source code, Cicada's Onions have precisely had quite small source code.
- The work is distributed over many separate computers. If, say, 10,000 people use this website, the amount of time needed to find the DWH is decreased by a factor of 10,000 as we can compute 10,000 times more hashes a second.
- Individual computers may have more processing power. Some supercomputers have millions of cores, which would enable them to hash trillions of bytes a second. It's unlikely, however, that we could access such a supercomputer.

Another contrasting downside is that the first string which hashes to the DWH may not be the intended string. Such collisions are doomed to happen: there are infinitely many inputs but only finitely many outputs, so the pigeonhole principle applies. Hence, we won't stop the search once the DWH has first occurred. But searching for collisions is marginally faster than searching for preimages, and we will likely have a few collisions before all hashes have been found.

# Mechanism

On the page to contribute, you will choose a hash algorithm with which to search (after all, the DWH might be something other than SHA-512). The server then assigns your computer a section of the hashes to work on, which it will do locally. It likely won't take long; the use of these sections is so that multiple computers don't overlap, as this is a waste of productivity. Currently it doesn't work: the code hasn't been written and it would likely require server-side code, while GitHub pages only supports static sites. Eventually something will be figured out... Then the search for the DWH can commence!

# Contribute

[Contribute](compute.md) your computer power to find the DWH!
