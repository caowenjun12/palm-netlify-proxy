curl https://{glittery-semolina-0b6a1c.netlify.app}/v1/models/gemini-pro:generateContent?key={AIzaSyAD7CF60ZdCAItBXuQBZRlMEn7Ep--orm8} \
   -H 'Content-Type: application/json' \
   -X POST \
   -d '{ "contents":[
   { "parts":[{"text": "Hi"}]}
   ]
}'

curl https://{glittery-semolina-0b6a1c.netlify.app}/v1/models/gemini-pro:streamGenerateContent?key={AIzaSyAD7CF60ZdCAItBXuQBZRlMEn7Ep--orm8}&alt=sse \
   -H 'Content-Type: application/json' \
   --no-buffer \
   -d '{ "contents":[
         {"role": "user",
            "parts":[{"text": "Hi"}]
         }
         ]
      }' > response.json
