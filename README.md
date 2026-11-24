# Mihir Group – Vendor Portal

Vendor onboarding & KYC, BOQ/RFQ, quote comparison (3 rounds + final), PO approval, GRN, 3-way bill match, payments and vendor-wise ledger.

Static single-page app (`index.html`) + `supabase.js` (supabase-js 2.49.4 UMD, vendored).

Data: Supabase project `Mihir-Vendor-Portal` (ap-south-1), table `public.vp_records` (coll, id, data jsonb, ord) with realtime. Every change syncs live to all open devices.

**Demo security:** RLS policies currently allow the public site key to read/write `vp_records`, and sign-in has no password. Do not put real bank/KYC data in until Supabase Auth + per-role RLS is added.

Add `?local` to the URL to run offline with browser-only storage.
