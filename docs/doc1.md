---
id: doc1
title: QueryPie Install Guide
sidebar_label: QueryPie Brief Architecture
---
# 1. QueryPie

## 1.1 Brief Architecture
* 단순한 구조를 지향하고 있습니다. 

## 1.2 Components
* 설명

| 컴포넌트 명 | 설명 |
| :---: | :---: |
|   QueryPie Api| Rest Api 서버  & Admin|
|   QueryPie App| QueryPie의 Web Client   |
|   QueryPie DB| QueryPie 가 metadata들을 관리하는 DB  |

# 2. QueryPie DB 설치

## 2.1 개요
* QueryPie 에서는 관리할 Database 들의 metadata를 저장하기 위하여 MySQL 서버를 필요로함
* mysql 5.7 권장
* 설치 및 업그레이드시 Table Schema 들을 적용하기 위하여 DDL, DML권한이 핑요

## 2.2 User 및 DB 생성 예제 
```mysql
CREATE USER 'querypie'@'%' IDENTIFIED BY 'password';

CREATE database querypie CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci;

GRANT ALL privileges ON querypie.* TO querypie@'%';
```

# 3. QueryPie Docker Registry

## 3.1 개요
 * QueryPie의 컴포넌트들은 Private Docker Registry에서 관리 됨
 * Registry : dockerpie.querypie.com
 * 인증 정보는 설치 가이드와 함께 전달 됨

# 4. QueryPie 배포 - (Sole Docker Environment)

Nulla facilisi. Maecenas sodales nec purus eget posuere. Sed sapien quam, pretium a risus in, porttitor dapibus erat. Sed sit amet fringilla ipsum, eget iaculis augue. Integer sollicitudin tortor quis ultricies aliquam. Suspendisse fringilla nunc in tellus cursus, at placerat tellus scelerisque. Sed tempus elit a sollicitudin rhoncus. Nulla facilisi. Morbi nec dolor dolor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Cras et aliquet lectus. Pellentesque sit amet eros nisi. Quisque ac sapien in sapien congue accumsan. Nullam in posuere ante. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Proin lacinia leo a nibh fringilla pharetra.

# 5. QueryPie 배포 - ECS 

Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin venenatis lectus dui, vel ultrices ante bibendum hendrerit. Aenean egestas feugiat dui id hendrerit. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Curabitur in tellus laoreet, eleifend nunc id, viverra leo. Proin vulputate non dolor vel vulputate. Curabitur pretium lobortis felis, sit amet finibus lorem suscipit ut. Sed non mollis risus. Duis sagittis, mi in euismod tincidunt, nunc mauris vestibulum urna, at euismod est elit quis erat. Phasellus accumsan vitae neque eu placerat. In elementum arcu nec tellus imperdiet, eget maximus nulla sodales. Curabitur eu sapien eget nisl sodales fermentum.

# 6. QueryPie 배포 - EKS

Phasellus pulvinar ex id commodo imperdiet. Praesent odio nibh, sollicitudin sit amet faucibus id, placerat at metus. Donec vitae eros vitae tortor hendrerit finibus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Quisque vitae purus dolor. Duis suscipit ac nulla et finibus. Phasellus ac sem sed dui dictum gravida. Phasellus eleifend vestibulum facilisis. Integer pharetra nec enim vitae mattis. Duis auctor, lectus quis condimentum bibendum, nunc dolor aliquam massa, id bibendum orci velit quis magna. Ut volutpat nulla nunc, sed interdum magna condimentum non. Sed urna metus, scelerisque vitae consectetur a, feugiat quis magna. Donec dignissim ornare nisl, eget tempor risus malesuada quis.
