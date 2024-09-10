### Step 1 : Create a bucket in Amazon S3
   - give a global unique bucket name as a website page, region, and
   - select ACLs enabled to restrict access. ACLs are access control lists.
   - Choose Bucket owner preferred under Object Ownership.
   -  Public access to buckets is blocked by default. Because the files in your static website will need to be accessible through the internet, you must permit public access.
   - Enable Bucket Versioning, so like a version history
     
### Step 2:  Upload website content to your bucket
create an index.html,  and a folder with css, images and other contents of code you have in
 Create a folder or get a zip file you've downloaded. Unzip the file if you downloaded it.

 Upload the index.html as a file, an then add folder with the contents folder.
Return to the Amazon S3 console with your bucket page open. 
```
Choose the Objects tab.
Choose Upload
Choose Add files
Choose index.html
Choose Add folder
Choose the unzipped folder - NOT the zip file itself!
You might get a popup that tells you that all files in that folder will be uploaded.
Choose Upload
```
S3 will get to work right away!

### Step 3 :Configure a static website on Amazon S3

We have to  set up the bucket for static website hosting because S3 can be used for so many solutions other than web hosting.
