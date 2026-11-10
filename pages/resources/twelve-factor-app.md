---
layout: default
title: The Twelve-Factor App
permalink: /resources/the-twelve-factor-app
---
<!-- Styled Markdown: requires a renderer that permits HTML and inline CSS.
     GitHub and other sanitizing renderers may remove colors and layout styles.
     Card order follows the PDF: read down each column (01–04, 05–08, 09–12).
     Edit the text directly below; no external assets or fonts are required. -->

<div style="max-width:1200px;margin:24px auto;background:#EDF2F8;color:#23364A;font-family:Arial,Helvetica,sans-serif;line-height:1.45;border-radius:12px;overflow:hidden;">
<header style="background:#10243A;padding:28px 30px 25px;color:#FFFFFF;">
<p style="margin:0 0 12px;color:#6FE0D5;font-size:12px;font-weight:700;letter-spacing:1.8px;">ENGINEERING REFERENCE / CLOUD APPLICATIONS</p>
<h1 style="margin:0 0 10px;padding:0;border:0;color:#FFFFFF;font-size:36px;font-weight:800;line-height:1.15;">The Twelve-Factor App</h1>
<p style="margin:0;color:#E1EAF2;font-size:14px;">Portable code. Explicit configuration. Replaceable processes. Predictable releases.</p>
</header>
<table role="presentation" style="width:100%;margin:0;border:0;border-collapse:collapse;table-layout:fixed;"><tbody><tr style="border:0;"><td bgcolor="#14BCB3" style="height:4px;padding:0;border:0;background:#14BCB3;"></td><td bgcolor="#8174F4" style="height:4px;padding:0;border:0;background:#8174F4;"></td><td bgcolor="#F2AD54" style="height:4px;padding:0;border:0;background:#F2AD54;"></td></tr></tbody></table>
<div style="padding:14px 18px 20px;">
<table role="presentation" style="width:100%;table-layout:fixed;border-collapse:separate;border-spacing:10px 12px;margin:0;border:0;background:transparent;">
<tbody>
<tr style="background:transparent;border:0;">
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#E5F5F3;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#007F86;color:#FFFFFF;font-size:12px;vertical-align:middle;">01</span>Codebase</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>One codebase in version control; many deploys.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Deploy the same application repository to dev, staging and production. Each independently deployable app has its own codebase; share code as libraries.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#007F86;">Avoid:</strong> Separate repositories per environment; untracked production edits.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#F0EDFC;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#6550CC;color:#FFFFFF;font-size:12px;vertical-align:middle;">05</span>Build, release, run</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Strictly separate build, release and run stages.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Build an artifact; combine it with config into an identified release; run that release. Preserve releases for repeatable deploys and rollback.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#6550CC;">Avoid:</strong> Compiling or editing application code inside a live deployment.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#FFF3E2;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#B36A14;color:#FFFFFF;font-size:12px;vertical-align:middle;">09</span>Disposability</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Start quickly and shut down gracefully.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">On termination, stop accepting work and drain within the grace period. Finish or release jobs safely; design retries to avoid duplicate effects.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#B36A14;">Avoid:</strong> Assuming processes never die; losing work on abrupt shutdown.</p>
</div>
</td>
</tr>
<tr style="background:transparent;border:0;">
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#E5F5F3;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#007F86;color:#FFFFFF;font-size:12px;vertical-align:middle;">02</span>Dependencies</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Explicitly declare and isolate dependencies.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Use a manifest plus lockfile where supported, and an isolated runtime. Declare required system tools as well as language packages.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#007F86;">Avoid:</strong> Relying on globally installed packages or server-specific tooling.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#F0EDFC;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#6550CC;color:#FFFFFF;font-size:12px;vertical-align:middle;">06</span>Processes</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Run stateless, share-nothing processes.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Persist durable data in backing services. Use local disk and memory only for temporary work; store sessions outside individual processes.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#6550CC;">Avoid:</strong> Sticky in-memory sessions; user uploads on ephemeral disk.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#FFF3E2;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#B36A14;color:#FFFFFF;font-size:12px;vertical-align:middle;">10</span>Dev/prod parity</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Keep environments as similar as practical.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Minimize gaps in time, people and tools. Match backing-service types and versions; deploy small changes frequently through consistent workflows.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#B36A14;">Avoid:</strong> A different local database engine masking production behavior.</p>
</div>
</td>
</tr>
<tr style="background:transparent;border:0;">
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#E5F5F3;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#007F86;color:#FFFFFF;font-size:12px;vertical-align:middle;">03</span>Config</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Store deployment configuration in the environment.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Inject credentials, service URLs and deploy-specific settings at runtime. Use granular variables; secret managers can supply sensitive values.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#007F86;">Avoid:</strong> Secrets in Git; large environment-specific config bundles.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#F0EDFC;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#6550CC;color:#FFFFFF;font-size:12px;vertical-align:middle;">07</span>Port binding</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Export services through port binding.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">The app binds a port with its runtime or bundled server. A platform or reverse proxy routes requests to it; use the assigned port if provided.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#6550CC;">Avoid:</strong> Depending on a manually configured external application server.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#FFF3E2;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#B36A14;color:#FFFFFF;font-size:12px;vertical-align:middle;">11</span>Logs</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Treat logs as event streams.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Write events to stdout; the environment collects, routes and stores them. Structured fields and correlation IDs improve diagnosis.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#B36A14;">Avoid:</strong> App-managed rotating log files; credentials or tokens in logs.</p>
</div>
</td>
</tr>
<tr style="background:transparent;border:0;">
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#E5F5F3;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#007F86;color:#FFFFFF;font-size:12px;vertical-align:middle;">04</span>Backing services</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Treat backing services as attached resources.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Address databases, queues, caches and mail services through configuration. Swap compatible resources without changing application code.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#007F86;">Avoid:</strong> Hard-coded endpoints; treating a local database as special.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#F0EDFC;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#6550CC;color:#FFFFFF;font-size:12px;vertical-align:middle;">08</span>Concurrency</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Scale out through the process model.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Define process types, such as web and worker. Add instances of each independently. Let the execution environment supervise processes.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#6550CC;">Avoid:</strong> One giant process that couples web traffic and background jobs.</p>
</div>
</td>
<td valign="top" bgcolor="#FFFFFF" style="width:33.333%;padding:0;vertical-align:top;border:1px solid #FFFFFF;border-radius:8px;background:#FFFFFF;box-shadow:1px 2px 0 #DDE5EF;overflow:hidden;">
<h2 style="margin:0;padding:10px 12px;border:0;border-radius:7px 7px 0 0;background:#FFF3E2;color:#10243A;font-size:16px;font-weight:700;line-height:1.45;"><span style="display:inline-block;margin-right:8px;padding:2px 7px;border-radius:4px;background:#B36A14;color:#FFFFFF;font-size:12px;vertical-align:middle;">12</span>Admin processes</h2>
<div style="padding:11px 12px 13px;font-size:12px;">
<p style="margin:0 0 7px;color:#23364A;"><strong>Run admin tasks as one-off processes.</strong></p>
<p style="margin:0 0 7px;color:#23364A;">Run migrations, consoles and maintenance with the application release, config and dependencies. Version admin code alongside app code.</p>
<p style="margin:0;color:#23364A;"><strong style="color:#B36A14;">Avoid:</strong> Ad hoc scripts with different credentials or dependency versions.</p>
</div>
</td>
</tr>
</tbody>
</table>
<aside style="margin:10px 10px 0;padding:13px 16px;border-left:4px solid #12BBB0;border-radius:5px;background:#10243A;color:#FFFFFF;font-size:12px;">
<p style="margin:0 0 8px;color:#FFFFFF;"><strong style="color:#6FE0D5;letter-spacing:0.6px;">RELEASE FLOW</strong><br>Source + declared dependencies → Build artifact → Artifact + config = release → Run process types</p>
<p style="margin:0;color:#FFFFFF;"><strong style="color:#6FE0D5;letter-spacing:0.6px;">QUICK CHECK</strong><br>Fresh checkout builds? &nbsp;•&nbsp; Secrets external? &nbsp;•&nbsp; Restart loses no durable data? &nbsp;•&nbsp; Scale without shared local state? &nbsp;•&nbsp; Shutdown safe?</p>
</aside>
<footer style="padding:14px 10px 0;color:#526477;font-size:10px;">
<p style="margin:0 0 5px;">Source: <a href="https://12factor.net/" style="color:#007F86;">12factor.net</a> · Original methodology by Heroku engineers · Practical examples are implementation guidance.</p>
<p style="margin:0 0 12px;">Scope: deployment and operations principles; complement with security, backups, metrics/traces, and safe schema migration design.</p>
<p style="margin:0;text-align:right;"><a href="/assets/downloads/twelve-factor-app-refcard.pdf" style="color:#526477;font-size:11px;font-weight:700;text-decoration:none;">Downloaded a PDF version</a></p>
</footer>
</div>
</div>
