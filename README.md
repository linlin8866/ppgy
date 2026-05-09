多协议加出口ip

bash <(curl -Ls https://raw.githubusercontent.com/linlin8866/ppgy/main/ip.sh)


wget -qO- --no-check-certificate https://raw.githubusercontent.com/linlin8866/ppgy/main/ip.sh | bash


bash <(curl -fsSL https://raw.githubusercontent.com/hxzlplp7/sb-psiphon/main/install.sh)

bash <(wget -qO- https://raw.githubusercontent.com/hxzlplp7/sb-psiphon/main/install.sh)

vpsmenu


# 查看 Psiphon 状态
psictl status

# 切换出口国家
psictl country US
psictl country JP
psictl country AUTO    # 自动选择最佳出口

# 测试当前出口 IP
psictl egress-test

# 批量测试国家可用性
psictl country-test US JP SG DE FR GB

# 测试所有常用国家（28个）
psictl country-test-all

# 重启所有服务
psictl restart

# 查看分享链接（用于客户端导入）
psictl links

# 智能切换出口（先测试后选择可用国家）
psictl smart-country

# 查看日志
psictl logs          # 全部
psictl logs sb       # sing-box (VLESS/REALITY/AnyTLS)
psictl logs hy2      # hysteria2
psictl logs tuic     # tuic
psictl logs anytls   # anytls (sing-box)
