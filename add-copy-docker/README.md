## ADD vs COPY

| Feature                 | COPY                           | ADD                                          |
|-------------------------|--------------------------------|----------------------------------------------|
| File Transfer           | Copies files from build context | Copies files from build context              |
| Tar Archive Extraction  | No                             | Yes (automatically extracts .tar files)      |
| URL Support             | No                             | Yes (can fetch files from the web)           |
| Performance             | Faster, less overhead          | Can be slower if using additional features   |
| Security                | Safer for local file transfers | Can introduce risks when fetching from URLs  |
| Use Case                | Preferred for all local file copies | Use only for tar extraction or URL fetching |

