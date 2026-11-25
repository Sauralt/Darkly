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

| Vulnerability | Flag | Explanation |
| --- | --- | --- |
| [1 - Reset Password | FLAG{r3s3t_t0k3n_w4s_just_md5_lol} | [Details](<1 - reset password/explanation.md>) |
| 2 - PHP injection in profile picture | FLAG{unr3str1ct3d_upl0ad_g0_brrr} | [Details](<2 - malicious file upload/explanation.md>) |
| 3 - IDOR private notes | FLAG{1d0r_ur_pr0f1l3_1s_m1n3} | [Details](<3 - IDOR private notes/explanation.md>) |
| 4 - API project access | FLAG{md5_Is_4_n4m3pl4t3_n0t_4_l0ck} | [Details](<4 - API endpoint access/explanation.md>) |
| 5 - PATCH HTTP method | FLAG{just_p4tch_y0ur_0wn_r0l3_lol} | [Details](<5 - PATCH method http/explanation.md>) |
| 6 - XML injection | FLAG{d3fus3dxml_n3xt_spr1nt_pr0m1s3} | [Details](<6 - injection XML/explanation.md>) |
| 7 - God permissions on database | FLAG{th3_und3rsc0r3_sl4sh_kn0ws_th3_w4y} | [Details](<7 - god permission on database/explanation.md>) |

| Vulnerability | Explanation |
| --- | --- |
| 1 - JWT leak in sources comments | [Details](<1 - JWT in comments/explanation.md>) |
| 2 - Use of JWT to impersonate an existing account like admins | [Details](<2 - JWT not secured/explanation.md>) |
| 3 - No strong password policy and leaked md5 hashed passwords in admin panel | [Details](<3 - Bad Password + leaked md5 hash/explanation.md>) |
| 4 - No lock on password error | [Details](<4 - No lock for connecting/explanation.md>) |
