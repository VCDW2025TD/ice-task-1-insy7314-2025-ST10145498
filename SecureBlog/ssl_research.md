# Reflection on Adding HTTPS

1. **Did adding HTTPS change how your app behaves?**  
   Adding HTTPS changed how the browser communicates with my backend and frontend. The app now uses encrypted connections, and I noticed initial browser warnings because of the self-signed certificate.

2. **Were there any setup issues or certificate trust problems?**  
   Yes, at first the browser flagged the connection as “Not Secure” due to the self-signed certificate. After importing the certificate into Trusted Root Authorities, the warnings were reduced.

3. **What would need to change for a production deployment?**  
   For production, I would not use a self-signed certificate. Instead, I would use a trusted CA such as Let’s Encrypt, and likely configure SSL termination on a web server or cloud service (like Nginx, Netlify, or Vercel). This ensures proper trust and scalability.
