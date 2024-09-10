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

If you're not sure, choose buckets on the left hand side navigation bar, and then choose the bucket you created for this project.
Choose the Properties tab.
Scroll allllllllll the way down to the Static website hosting panel.
Choose Edit
Configure the following settings:
Static web hosting: Choose Enable
Hosting type: Choose Host a static website

Index document: Enter index.html

Choose Save changes
```
Under Properties,
In the Static website hosting panel
 under bucket website endpoint,
 click on the URL.
```
An error! 👀

The error message you're seeing is telling you that your static website is being hosted by S3, but the actual HTML/image files you've uploaded are still private. It's kind of like having a bucket on display, so everyone can see the bucket - but the contents are covered up, preventing anyone from seeing what's inside.

To solve this error, we need to set the permission of the objects to public - this is why we enabled ACLs in Task 1!

### step 4: Use ACLs to make objects in your S3 bucket public

Let's make the uploaded objects publicly accessible so users can view your website.


Would you still remember how to view your S3 bucket's objects? Try finding your bucket's 
 page and making your objects public using ACLs.

````
select bucket.
check all list of objects in bucket
Select the checkboxes of index.html file and the folder of website assets.
In the Actions dropdown,
choose Make public using ACL.

```

With this we make *** only the html file public, not the folder***. that's private.

### step 5: Delete Resources.

Empty buckets by deleting the objects in the bucket, Then we delete the Bucket.

