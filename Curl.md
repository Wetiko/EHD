# Curl

Here's a list of commonly used `curl` commands with their descriptions:

1. Send an HTTP GET request to a URL and display the response:
   ```
   curl <URL>
   ```

2. Fetch only the response headers of a URL:
   ```
   curl -I <URL>
   ```

3. Fetch both the response headers and the response body of a URL:
   ```
   curl -i <URL>
   ```

4. Send a POST request with data to a URL:
   ```
   curl -d "key1=value1&key2=value2" -X POST <URL>
   ```

5. Send a JSON POST request with data to a URL:
   ```
   curl -d '{"key1":"value1","key2":"value2"}' -H "Content-Type: application/json" -X POST <URL>
   ```

6. Follow redirects and display the final URL:
   ```
   curl -L <URL>
   ```

7. Specify a custom User-Agent header in the request:
   ```
   curl -A "User-Agent-String" <URL>
   ```

8. Download a file from a URL and save it locally:
   ```
   curl -O <URL>
   ```

9. Download a file from a URL and save it with a specific name:
   ```
   curl -o <filename> <URL>
   ```

10. Resume a previously interrupted file download:
    ```
    curl -C - -o <filename> <URL>
    ```

11. Upload a file to a remote server using HTTP POST:
    ```
    curl -F "file=@<filename>" <URL>
    ```

12. Set a cookie for the request:
    ```
    curl -b "name=value" <URL>
    ```

13. Include the Referer header in the request:
    ```
    curl -e "<referrer-url>" <URL>
    ```

14. Limit the maximum time allowed for the request:
    ```
    curl --max-time <seconds> <URL>
    ```

15. Ignore SSL certificate verification:
    ```
    curl -k <URL>
    ```

16. Save verbose output to a file:
    ```
    curl -o <output-file> -v <URL>
    ```

17. Limit the rate of data transfer:
    ```
    curl --limit-rate <rate> <URL>
    ```

18. Send a request with a specific HTTP method (e.g., PUT, DELETE):
    ```
    curl -X <HTTP-method> <URL>
    ```

19. Send a request with a specific header:
    ```
    curl -H "Header-Name: value" <URL>
    ```

20. Send a request with Basic Authentication credentials:
    ```
    curl -u "<username>:<password>" <URL>
    ```

These are some commonly used `curl` commands that cover a range of HTTP request scenarios. The specific options and usage may vary depending on your requirements and the specific API or web service you are interacting with. You can refer to the `curl` manual or command documentation for more detailed information on the available options and their usage.

# Examples

Here are some examples of `curl` commands with their usage:

1. Send an HTTP GET request to a URL and display the response:
   ```
   curl https://api.example.com
   ```

2. Fetch only the response headers of a URL:
   ```
   curl -I https://api.example.com
   ```

3. Fetch both the response headers and the response body of a URL:
   ```
   curl -i https://api.example.com
   ```

4. Send a POST request with data to a URL:
   ```
   curl -d "key1=value1&key2=value2" -X POST https://api.example.com
   ```

5. Send a JSON POST request with data to a URL:
   ```
   curl -d '{"key1":"value1","key2":"value2"}' -H "Content-Type: application/json" -X POST https://api.example.com
   ```

6. Follow redirects and display the final URL:
   ```
   curl -L https://example.com
   ```

7. Specify a custom User-Agent header in the request:
   ```
   curl -A "My User Agent" https://api.example.com
   ```

8. Download a file from a URL and save it locally:
   ```
   curl -O https://example.com/file.txt
   ```

9. Download a file from a URL and save it with a specific name:
   ```
   curl -o localfile.txt https://example.com/file.txt
   ```

10. Resume a previously interrupted file download:
    ```
    curl -C - -o file.txt https://example.com/file.txt
    ```

11. Upload a file to a remote server using HTTP POST:
    ```
    curl -F "file=@localfile.txt" https://api.example.com/upload
    ```

12. Set a cookie for the request:
    ```
    curl -b "name=value" https://api.example.com
    ```

13. Include the Referer header in the request:
    ```
    curl -e "https://referer.example.com" https://api.example.com
    ```

14. Limit the maximum time allowed for the request:
    ```
    curl --max-time 10 https://api.example.com
    ```

15. Ignore SSL certificate verification:
    ```
    curl -k https://api.example.com
    ```

16. Save verbose output to a file:
    ```
    curl -o output.txt -v https://api.example.com
    ```

17. Limit the rate of data transfer:
    ```
    curl --limit-rate 100K https://api.example.com
    ```

18. Send a request with a specific HTTP method (e.g., PUT, DELETE):
    ```
    curl -X PUT https://api.example.com/resource
    ```

19. Send a request with a specific header:
    ```
    curl -H "Authorization: Bearer token123" https://api.example.com
    ```

20. Send a request with Basic Authentication credentials:
    ```
    curl -u "username:password" https://api.example.com
    ```

These examples showcase various scenarios where `curl` can be used to interact with different APIs and web services. Modify the URLs, data, and headers as per your specific use case.