```mermaid
flowchart LR
    A[Ubuntu / Apache Server / MariaDB]
    B[Web Host]
    C[DB Host]
    D[Firewall]
    E[syslog]
    F[Splunk]
    G[Dashboard]

    %% 連線示意
    A --> B
    A --> C
    B --> D
    C --> D

    %% 日誌傳送
    B --> E
    C --> E
    E --> F
    F --> G
