# Network Fundamentals – README

Aşağıda, LinkedIn açıklaması ve sınav/soru kısmına geçmeden önce öğrenilen tüm konular **başlıklar halinde**, **Türkçe – İngilizce karşılıklı tablo** formatında özetlenmiştir.

---

## 1. OSI Modeli

| Türkçe                                                                                 | English                                                                                         |
| -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| OSI modeli, ağ iletişimini 7 katmana ayıran kavramsal bir referans modelidir.          | The OSI model is a conceptual reference model that divides network communication into 7 layers. |
| Katmanlar: Physical, Data Link, Network, Transport, Session, Presentation, Application | Layers: Physical, Data Link, Network, Transport, Session, Presentation, Application             |
| Gerçek bir sistem değil, öğrenme ve standartlaştırma amaçlıdır.                        | It is not a real system but used for learning and standardization.                              |

---

## 2. TCP/IP Modeli

| Türkçe                                                               | English                                                                        |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| TCP/IP modeli, internetin temelini oluşturan pratik ağ modelidir.    | TCP/IP is the practical networking model that forms the basis of the internet. |
| 4 katmandan oluşur: Network Access, Internet, Transport, Application | Consists of 4 layers: Network Access, Internet, Transport, Application         |
| OSI modeline göre daha sade ve gerçekte kullanılandır.               | It is simpler than OSI and used in real-world networks.                        |

---

## 3. TCP ve UDP

| Türkçe                                        | English                                      |
| --------------------------------------------- | -------------------------------------------- |
| TCP bağlantı odaklıdır ve güvenilirdir.       | TCP is connection-oriented and reliable.     |
| UDP bağlantısızdır ve daha hızlıdır.          | UDP is connectionless and faster.            |
| TCP veri bütünlüğünü garanti eder, UDP etmez. | TCP guarantees data integrity, UDP does not. |

---

## 4. IP Adresleme (IPv4 / IPv6)

| Türkçe                                                              | English                                                         |
| ------------------------------------------------------------------- | --------------------------------------------------------------- |
| IP adresi, bir cihazın ağ üzerindeki mantıksal kimliğidir.          | An IP address is the logical identity of a device on a network. |
| IPv4 32-bit, IPv6 128-bit adresleme kullanır.                       | IPv4 uses 32-bit, IPv6 uses 128-bit addressing.                 |
| IPv6, daha fazla adres ihtiyacını karşılamak için geliştirilmiştir. | IPv6 was developed to handle address exhaustion.                |

---

## 5. MAC Adresi ve Ethernet

| Türkçe                                                            | English                                                             |
| ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| MAC adresi, cihazın fiziksel adresidir.                           | A MAC address is the physical address of a device.                  |
| Ethernet, yerel ağlarda kullanılan temel iletişim teknolojisidir. | Ethernet is the primary communication technology in local networks. |
| IP mantıksal, MAC fiziksel adresleme yapar.                       | IP is logical, MAC is physical addressing.                          |

---

## 6. DNS (Domain Name System)

| Türkçe                                             | English                                                     |
| -------------------------------------------------- | ----------------------------------------------------------- |
| DNS, alan adlarını IP adreslerine çevirir.         | DNS translates domain names into IP addresses.              |
| Kullanıcıların IP yerine isimle erişmesini sağlar. | Allows users to access services using names instead of IPs. |
| İnternetin temel servislerinden biridir.           | It is a core internet service.                              |

---

## 7. Port Numaraları

| Türkçe                                             | English                                            |
| -------------------------------------------------- | -------------------------------------------------- |
| Portlar, aynı IP üzerindeki servisleri ayırt eder. | Ports distinguish services on the same IP address. |
| Örnek: HTTP 80, HTTPS 443                          | Example: HTTP 80, HTTPS 443                        |
| TCP ve UDP ile birlikte kullanılır.                | Used together with TCP and UDP.                    |

---

## 8. URL, URI, URN

| Türkçe                           | English                                   |
| -------------------------------- | ----------------------------------------- |
| URI genel tanımlayıcıdır.        | URI is the general identifier.            |
| URL, kaynağın adresini belirtir. | URL specifies the location of a resource. |
| URN, kaynağın ismini belirtir.   | URN specifies the name of a resource.     |

---

## 9. Kablosuz Ağlar (Wi-Fi)

| Türkçe                                               | English                                          |
| ---------------------------------------------------- | ------------------------------------------------ |
| Wi-Fi, radyo dalgaları ile veri iletir.              | Wi-Fi transmits data using radio waves.          |
| Fiziksel kablo yoktur ancak donanımsal alıcı vardır. | No physical cable, but hardware receivers exist. |
| Kablosuz olsa da fiziksel katman mevcuttur.          | Even wireless networks have a physical layer.    |

---

## 10. Cisco Packet Tracer

| Türkçe                                                                      | English                                                          |
| --------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Packet Tracer, Cisco tarafından geliştirilen ağ simülasyon aracıdır.        | Packet Tracer is a network simulation tool developed by Cisco.   |
| Eğitmen tarafından yapılan uygulamalar takip edilerek öğrenme pekiştirildi. | Learning was reinforced by following instructor-led simulations. |
| Gerçek ağ senaryolarını risksiz ortamda gösterir.                           | Demonstrates real network scenarios in a safe environment.       |

---

## 11. Frontend ile Ağ Temelleri İlişkisi

| Türkçe                                                       | English                                                                |
| ------------------------------------------------------------ | ---------------------------------------------------------------------- |
| Frontend uygulamalar istemci–sunucu iletişimine dayanır.     | Frontend applications rely on client–server communication.             |
| HTTP, TCP/IP ve DNS bilgisi daha bilinçli geliştirme sağlar. | Knowledge of HTTP, TCP/IP, and DNS enables more conscious development. |
| Performans ve hata analizinde ağ bilgisi önemlidir.          | Network knowledge is important for performance and error analysis.     |

---

> Bu README, BTK Akademi Ağ Temelleri eğitimi kapsamında öğrenilen temel network kavramlarının özetidir.
