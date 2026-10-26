HUONG DAN CHAY BOT TREN INJECTCLOUD

1) Tai len ZIP nay bang Dashboard > New App > ZIP (hoac upload vao app hien co roi Rebuild).
   ZIP co main.py va requirements.txt ngay o thu muc goc.
2) Mo app > Environment va them cac bien can thiet:
   - BOT_TOKEN: token moi vua tao lai bang @BotFather.
   - KEY_SERVER_URL: URL server cap key (mac dinh trong .env.example).
   - KEY_SERVER_ADMIN_SECRET: secret dung chung voi server cap key.
   - ADMIN_CHAT_IDS: danh sach Telegram ID admin, cach nhau bang dau phay.
3) Tren server cap key (vi du Render), doi secret server sang mot gia tri moi va dat cung gia tri do
   cho KEY_SERVER_ADMIN_SECRET tren InjectCloud. Khong de secret that trong file ma nguon.
4) Giu cac bien thanh toan PAYMENT_WALLET, PAYMENT_ACCOUNT_NAME, PAYMENT_ACCOUNT_NUMBER dung voi
   thong tin nhan tien cua ban; chi can ghi de neu muon thay gia tri mac dinh trong code.
5) Bam Restart/Rebuild, sau do xem Console/Logs. Bot se chay bang Telegram long polling.

BAO MAT:
- File goc da co token bot va secret server viet truc tiep trong code. Hay thu hoi/tao lai token
  bot bang @BotFather, va thay secret server o ca hai noi nhu huong dan tren.
- Khong upload file .env co gia tri that len GitHub/ZIP cong khai. .env.example chi la mau.

LUU DU LIEU:
Bot ghi don, so du, pending va log vao cac file JSON trong BOT_DATA_DIR. Neu InjectCloud co
persistent storage/disk, hay dat BOT_DATA_DIR vao duong dan mount do; neu khong, du lieu tren dia
cuc bo co the khong duoc giu sau khi xoa app/rebuild tuy co che cua host.
