# Generating and download a file with contents

```PHP
return response($contents)
                ->withHeaders([
                    'Content-Type' => 'text/plain',
                    'Cache-Control' => 'no-store, no-cache',
                    'Content-Disposition' => 'attachment; filename="logs.txt',
                ]);
```
