# ansible-sssignal2.2
水飴信号の構成を管理するansible！

## 環境
| ミドルウェア | バージョン |
|-----------|------------|
| Ansible | 2.6.3 |
| Virtualbox | 5.2.18 |
| Vagrant | 2.1.2 |
| PHP | 7.2 |
| MongoDB | 3.6.7 |

## 使い方
git clone https://github.com/mizzsig/ansible-sssignal2.2.git
cd ansible-sssignal2-2
git clone https://github.com/mizzsig/sssignal2.2.git
vi sssignal2-2/.env
vagrant up 
vagrant ssh

## TODO
 - [ ] 冪等性を担保する
 - [ ] bashの設定いい感じにする