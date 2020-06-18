
While developing Softphone application using VS 2008, I moved a project from one computer to a different one. When I then tried to rebuild the solution I received the following error:

&#8220; Unable to find manifest signing certificate in the certificate store &#8221;

As I was sure that I wasn&#8217;t using any certificate to sign the assembly I couldn&#8217;t understand the reason for this error message. It turned out that I had to manually go into the *.vbproj file and remove the following four lines that were apparently left over from some past experiments with signing using a certificate:

&#8230; manifestcertificatethumbprint &#8230;
&#8230; manifestkeyfile &#8230; 
&#8230; generatemanifests &#8230;  
&#8230; signmanifests &#8230;

After I had removed those lines I reloaded the project and the solution rebuilt just fine.
