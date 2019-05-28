# spring-config-server
Spring Cloud Config adalah salah satu feature dari Netflix yang memungkinkan configurasi di simpan di dalam server ini. Cara kerja dari Spring Config Server ini adalah pada saat server ini booting dia akan mencari bootstrap.properties yang memiliki property letak dari konfigurasi

# dependencies
config-server

# how to
1. Tambahkan <code>@EnableConfigServer</code> pada SpringBootApplication class, dgn konfigursi ini menandakan bila server ini akan di gunakan sebagi configurasi server, dan akan error bila property <code>spring.cloud.config.server.git.uri</code> tidak tersedia.
2. Buatlah bootstrap.properties selevel dengan application.properties. 
lalu isi dengan <code>spring.cloud.config.server.git.uri=https://github.com/elvinotan/config</code>
Konfigurasi ini menandakan pada saat server config ini hidup, please ambil konfigurasi di alamat <code>https://github.com/elvinotan/config</code>

