# Generating and download a file with contents

```PHP
return response($entry_code.$exit_code)
                ->withHeaders([
                    'Content-Type' => 'text/plain',
                    'Cache-Control' => 'no-store, no-cache',
                    'Content-Disposition' => 'attachment; filename="logs.txt',
                ]);
```
