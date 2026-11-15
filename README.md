# NetCut Clone (Termux)

Android ဖုန်း (Termux) အတွက် ရေးထားတဲ့ ကွန်ရက် Scan ဖတ်ခြင်းနှင့် ARP Spoofing Tool ဖြစ်ပါတယ်။ ဒီ Tool ကို အသုံးပြုပြီး ကွန်ရက်ထဲက Device တွေကို ရှာဖွေနိုင်တယ်၊ သူများရဲ့ အင်တာနက်လိုင်းကို နှေးစေတာ ဒါမှမဟုတ် လုံးဝ ဖြတ်တောက်တာတွေ လုပ်နိုင်ပါတယ်။

## ⚠️ သတိပေးချက် (DISCLAIMER)
**ဒီ Tool ကို ပညာရေးဆိုင်ရာ လေ့လာမှုနဲ့ ခွင့်ပြုချက်ရထားတဲ့ စမ်းသပ်မှုတွေအတွက်ပဲ အသုံးပြုရပါမယ်။** ကိုယ့်ပိုင်မဟုတ်တဲ့ ကွန်ရက်တွေ ဒါမှမဟုတ် ခွင့်ပြုချက်မရထားတဲ့ နေရာတွေမှာ လုံးဝ အသုံးမပြုရပါဘူး။ 

## လုပ်ဆောင်ချက်များ (Features)
- **Network Scan:** ကွန်ရက်ထဲမှာ ချိတ်ဆက်ထားတဲ့ Device တွေကို IP နဲ့ MAC ပါ ရှာဖွေပေးတယ်။
- **Speed Limit:** Target ဖုန်းရဲ့ အင်တာနက်ကို အလွန်နှေးသွားအောင် လုပ်ပေးတယ်။
- **Block Internet:** Target ဖုန်းရဲ့ အင်တာနက်ကို လုံးဝ ဖြတ်တောက်ပစ်တယ်။
- **Wi-Fi Killer:** ကွန်ရက်ထဲက Device အားလုံးကို တစ်ခါတည်း လိုင်းဖြတ်တယ်။

## လိုအပ်ချက်များ (Prerequisites)
မသုံးခင် အောက်ပါအချက်တွေ ရှိဖို့ လိုပါတယ် -
1. **Termux** သွင်းထားရမယ်။
2. **Root (su)** ရှိရမယ် (ARP Spoofing လုပ်ဖို့)။
3. **arpspoof** သွင်းထားရမယ်။

## သွင်းနည်း (Installation)

၁။ လိုအပ်တဲ့ Package များ သွင်းပါ:**
```bash
pkg update && pkg upgrade -y
pkg install python git root-repo -y
pip install rich

၂။ arpspoof သွင်းပါ (မရှိသေးရင်):

```bash
git clone https://github.com/CoolestEnoch/arpspoof-termux.git
cd arpspoof-termux/jni
gcc -I./include -lnet -lpcap *.c -o arpspoof
mv arpspoof $PREFIX/bin/
chmod +x $PREFIX/bin/arpspoof
cd ../..
rm -rf arpspoof-termux
```

၃။ ဒီ Repo ကို Clone လုပ်ပါ:

```bash
git clone https://github.com/sankyi10001122-spec/NetCut-Clone.git
cd NetCut-Clone
```

အသုံးပြုနည်း (Usage)

၁။ ဖိုင်ကို Run ခွင့်ပြုပါ:

```bash
chmod +x s
```

၂။ Root နဲ့ Run ပါ:

```bash
su
./s
```

၃။ Menu ပေါ်လာရင် လိုချင်တာကို ရွေးပါ:

· Target ရွေးချယ်ရန် Device နံပါတ်ကို ရိုက်ထည့်ပါ။
· မုဒ် 1 (MITM), 2 (Speed Limit), သို့မဟုတ် 3 (Block Internet) ကို ရွေးပါ။
· Device အားလုံးကို လိုင်းဖြတ်ချင်ရင် A ကို ရိုက်ပါ။
· ရပ်ချင်ရင် Ctrl + C နှိပ်ပြီး ကွန်ရက်ကို ပုံမှန်ပြန်ဖြစ်စေပါ။

မှတ်ချက်

· ဒီ Tool က Root ရှိတဲ့ ဖုန်းတွေမှာပဲ အလုပ်လုပ်ပါမယ်။
· စမ်းသပ်ပြီးတိုင်း Ctrl+C နှိပ်ပြီး ကွန်ရက်ကို ပြန်ကောင်းအောင် လုပ်ဖို့ မမေ့ပါနဲ့။



Tiktok Official - @zerotozero94
