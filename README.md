# dupeImageFinder

While looking for a way to get rid of duplicate images, I found several solutions. However, they were basically getting the 
MD5 hash of the file. This helped with strict duplicates, but not near dupes, like if an image is the same but different size or there is some other small change that would cause an "identical" image to have a different MD5.

So, doing some research, I stumbled upon hashing code that will create a hash from the image data itself.

The code I found is from a virus infected site (that I think is a mirror of a site that was originally in Chinese)
The "English" website is: http://www.developermemo.com/1262721/   (be careful going here! have your virus scanner ready!)

Anyway, the hashing code uses open cv to read files, but, it probably can be easily modified to work with any image loading lib.

The rest of the code is done in WinAPI (non-MFC). It uses a tree view to group similar images. Clicking on an entry will open the image for viewing.
