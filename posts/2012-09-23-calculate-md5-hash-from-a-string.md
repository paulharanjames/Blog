
It is a common practice to store passwords in databases using a hash. MD5 (defined in [RFC 1321](http://www.ietf.org/rfc/rfc1321.txt)) is a common hash algorithm, and using it from C# is easy. 

Here’s an implementation of a method that converts a string to an MD5 hash, which is a 32-character string of hexadecimal numbers.

<pre>public string CalculateMD5Hash(string input)<br />{<br />    // step 1, calculate MD5 hash from input<br />    MD5 md5 = System.Security.Cryptography.MD5.Create();<br />    byte[] inputBytes = System.Text.Encoding.ASCII.GetBytes(input);<br />    byte[] hash = md5.ComputeHash(inputBytes);<br /><br />    // step 2, convert byte array to hex string<br />    StringBuilder sb = new StringBuilder();<br />    for (int i = 0; i &lt; hash.Length; i++)<br />    {<br />        sb.Append(hash[i].ToString("X2"));<br />    }<br />    return sb.ToString();<br />}<br /></pre>



An example call:

<pre>string hash = CalculateMD5Hash("abcde123");</pre>



…returns a string like this:

<pre>C3FCD3D76192E4007DFB496CCA67E13B</pre>



To make the hex string use lower-case letters instead of upper-case, replace the single line inside the _for_ loop with this line:

<pre>sb.Append(hash[i].ToString("x2"));</pre>



The difference is the ToString method parameter.