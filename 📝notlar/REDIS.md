# Redis Hakkında notlar

## Redis Authentication

Redis'i kurduktan sonra, authenticate olmak için, terminalde şu kodlar çalıştırılmalıdır;

```bash
redic-cli
> ACL SETUSER <username> on ><password> ~* &* +@all
> CONFIG REWRITE
```

Bu komutların çalıştığını doğrulamak için;

```bash
redis-cli
> AUTH <username> <password>
```

Eğer hata vermediyse, başarılı bir şekilde terminalden kullanıcı ile authenticate olunabilmiştir demektir. Detaylı bilgi için [dokümantasyon](https://redis.io/docs/management/security/acl/) inceleyebilirsiniz.
