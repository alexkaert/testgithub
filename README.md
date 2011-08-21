Testing github connection
============

Sometimes when I want to push, I get

<pre>
ssh: Could not resolve hostname github.com: nodename nor servname provided, or not known
Alexs-MacBook-Pro:testgithub alexkaert$ ssh -T git@github.com
</pre>

I think it's a internet connection error.

A sketchy way to "solve" it:

1. Change your public key online, just delete a character and remember which character 
2. $ `ssh -T git@github.com`
3. If you get a public key denied error, that's good. If not keep doing step 2
4. Chnage you public key back to the correct one.
5. `ssh -T git@github.com` should work and give you the correct response, if not, repeat 1-4
6. `git push`, if this failed, repeat 1-5
