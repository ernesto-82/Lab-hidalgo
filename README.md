# Laboratorio "El Hidalgo de La Mancha"

Este repositorio contiene la configuración y documentación del laboratorio de red segmentada con Docker, MikroTik y OpenLDAP.

## 🏗️ Arquitectura

- **Router Frontera:** MikroTik (RouterOS) con NAT y firewall.
- **Host de Contenedores:** Debian 12 con Docker (IPvlan) y 11 contenedores (Admin, Ventas, Dirección, Informática, Invitados).
- **Servidor Central:** Ubuntu Server 22.04 con DNS (BIND9), DHCP, PostgreSQL, OpenLDAP y LAM.

## 🚀 Servicios Desplegados

- **Segmentación física:** Un cable virtual por red (Ventas, Informática, Servidor, Invitados).
- **Direccionamiento VLSM:** Subredes optimizadas para cada departamento.
- **Aislamiento:** Firewall en MikroTik que bloquea el acceso de Ventas a PostgreSQL.
- **Auditoría:** Capturas con `tcpdump` para demostrar la seguridad del cifrado.

## 📦 Instalación Rápida

1. Clona el repositorio:
   ```bash
   git clone https://github.com/ernesto-82/Lab-hidalgo.git
