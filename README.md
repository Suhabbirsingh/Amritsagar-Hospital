# Still needed from the hospital

- [x] Appointments are not handled through email; use the phone number or the booking system once connected.
- [ ] Data Protection Officer: this post has not been appointed yet; every footer states this.
- [ ] Connect the patient login, OTP, reports, bills, prescriptions and records APIs; [patient-login.html](patient-login.html) provides the static portal interface.
- [x] Logo and matching blue/green brand colours have been added.
- [ ] Confirm operating hours and preparation requirements for each service — [health-packages.html](health-packages.html).
- [ ] Confirm the cashless list remains current, plus government-scheme status and room tariffs ” [insurance.html](insurance.html).
- [ ] Confirm registration number, leadership, department hours, emergency capability, blood-bank details, all clinical content, reviewer credentials and dates.
- [ ] Confirm grievance designation and turnaround times, CIN/registration, DPO, legal policy content, remaining clinician details, years/languages/fees/NMC numbers.

# Amritsagar Hospital static site

Open `index.html` by double-clicking it. No install, server, network dependency, framework, or build step is needed.

## Simple edits

Change colours and fonts only in the `:root` block at the top of `assets/style.css`. Hospital name, address and phone details are repeated in every page header/footer: use project-wide search to update them in one pass. Confirmed details are: AMRITSAGAR HOSPITAL, SERVING HUMANITY, 2022, Baddi, 21 beds, 10+ departments/doctors, and 7832006300.

## Pages

| File | Purpose | Edit |
|---|---|---|
| index.html | Home | Hero, feature cards, articles |
| about.html | About | Mission, milestones, leadership |
| specialties.html | Directory | Department cards |
| specialty-cardiology.html | Specialty template | Duplicate then replace brackets |
| doctors.html | Directory | Confirmed doctor cards |
| doctor-profile.html | Doctor template | Duplicate then replace brackets |
| locations.html | Baddi location | Directions, map and facilities |
| emergency.html | Emergency | Confirm clinical capability |
| health-packages.html | Our Services | Service descriptions and hours |
| insurance.html | Insurance | Payers, tariffs and schemes |
| book-appointment.html | Booking shell | HIS handoff only |
| patient-login.html | Portal handoff | HIS links |
| contact.html | Contact and grievance | Directory and TATs |
| 404.html | Not found | Essential links |

## Add a doctor

1. Duplicate `doctor-profile.html` and rename it `doctor-firstname.html`.
2. Replace bracketed profile, qualification, NMC registration, schedule and fee fields with confirmed information.
3. Add a matching card in `doctors.html` linking to the new file.
4. Keep the NMC ethics comment; do not add testimonials or comparative claims.

## Add a specialty

1. Duplicate `specialty-cardiology.html` and rename it `specialty-name.html`.
2. Update title, H1, overview, treatments, timings, FAQ and clinician cards using approved clinical text.
3. Update the card in `specialties.html` and related home card.

## Integration points

| Name | Page | Need | Owner |
|---|---|---|---|
| appointment slots | book-appointment | HIS slots API | HIS integration team |
| appointment creation | book-appointment | appointment API | HIS integration team |
| payment gateway | booking | payment provider | HIS integration team |
| patient login/OTP | patient-login | HIS portal + OTP | HIS integration team |
| lab reports, bills, prescriptions | patient-login | HIS APIs | HIS integration team |
| ABDM/ABHA | booking | ABDM linking | HIS integration team |
| enquiry forms | contact/insurance | secure delivery | HIS integration team |
| careers/ATS | footer | careers page | hospital/web team |
| map embeds | locations | approved map | web team |
| bed/blood availability | emergency | live source | clinical/HIS team |

## Compliance checklist

- [ ] Finalise DPDP privacy notice, DPO and data-rights page.
- [ ] Verify consent records and data hosting in India before portal launch.
- [ ] Verify NMC-compliant clinician biographies.
- [ ] Verify PCPNDT notice and applicable ultrasound content.
- [ ] Verify Telemedicine Guidelines disclosures.
- [ ] Publish approved tariffs, patient rights and grievance turnaround times.
- [ ] Assign medical author/reviewer and review dates to medical information.

## Still to build

Blog, careers, news, patient rights, quality, international patients, blood bank and legal/policy pages currently route to `404.html`.

## Deployment

Any static host works: Netlify, Cloudflare Pages, GitHub Pages, or shared hosting. Once a patient portal is added, health data must be hosted in India.




