# Darkly — 42 Security Project

## Description

Darkly is an educational project from 42 focused on web security. The goal is to identify and exploit a set of vulnerabilities in an intentionally vulnerable application, within a controlled learning environment.

## Objective

Find and document all the security flaws present in the application, following a clear methodology for each one: discovery, proof of concept, impact, and proposed fix.

## Test environment

- **Target URL**: `http://localhost:XXXX`
- **Tools used**: browser (DevTools), curl

## Methodology

For each vulnerability found:

1. Identify the entry point (form, API endpoint, upload, etc.)
2. Confirm the flaw with a minimal proof of concept
3. Assess the impact (data read access, privilege escalation, code execution, etc.)
4. Document the exact payload used
5. Propose a remediation

## List of vulnerabilities found

| Vulnerability | Flag |
| --- | --- |
| 1 - Reset Password | FLAG{r3s3t_t0k3n_w4s_just_md5_lol} |
| 2 - PHP injection in profile picture | FLAG{unr3str1ct3d_upl0ad_g0_brrr} |
| 3 - IDOR private notes | FLAG{1d0r_ur_pr0f1l3_1s_m1n3} |
| 4 - API project access | FLAG{md5_Is_4_n4m3pl4t3_n0t_4_l0ck} |
| 5 - PATCH HTTP method | FLAG{just_p4tch_y0ur_0wn_r0l3_lol} |
| 6 - XML injection | FLAG{d3fus3dxml_n3xt_spr1nt_pr0m1s3} |
| 7 - God permissions on database | FLAG{th3_und3rsc0r3_sl4sh_kn0ws_th3_w4y} |

### Vulnerabilities without flags :
1 - JWT leak in sources comments

2 - Use of JWT to impersonate an existing account like admins

3 - No strong password policy and leaked md5 hashed passwords in admin panel

4 - No lock on password error

Everything is explained in each vulnerability 'explanation.md'.
