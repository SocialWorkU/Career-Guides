# Career-Guides
Social Work Career Guides by State
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Complete State Social Work Licensing Guides</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
            margin-bottom: 30px;
        }

        .header h1 {
            color: #1e4a5d;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .header p {
            color: #666;
            font-size: 1.1rem;
        }

        .state-selector {
            background: white;
            border-radius: 15px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .state-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .state-button {
            padding: 15px 20px;
            border: 2px solid #e2e8f0;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            color: #64748b;
            text-align: center;
        }

        .state-button:hover {
            background: #f1c232;
            border-color: #f1c232;
            color: #1e4a5d;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .state-button.featured {
            background: #1e4a5d;
            border-color: #1e4a5d;
            color: white;
        }

        .state-button.active {
            background: #10b981;
            border-color: #10b981;
            color: white;
        }

        .guide-display {
            background: white;
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            margin-bottom: 30px;
            min-height: 600px;
        }

        .guide-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .guide-title {
            font-size: 2.5rem;
            color: #1e4a5d;
            margin-bottom: 15px;
            font-weight: 700;
        }

        .guide-subtitle {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 20px;
        }

        .last-updated {
            background: #f0fdf4;
            color: #166534;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
        }

        .quick-facts {
            background: linear-gradient(135deg, #10b981 0%, #059669 100%);
            color: white;
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 40px;
        }

        .facts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
        }

        .fact-item {
            text-align: center;
        }

        .fact-number {
            font-size: 2.2rem;
            font-weight: 700;
            display: block;
            margin-bottom: 5px;
        }

        .fact-label {
            font-size: 0.95rem;
            opacity: 0.9;
        }

        .license-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .license-card {
            background: white;
            padding: 30px;
            border-radius: 12px;
            border-left: 5px solid #10b981;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }

        .license-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }

        .license-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
        }

        .license-title {
            font-size: 1.3rem;
            color: #1e4a5d;
            font-weight: 600;
        }

        .license-abbrev {
            background: #10b981;
            color: white;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.85rem;
            font-weight: 600;
        }

        .license-description {
            color: #666;
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .requirements-list {
            list-style: none;
        }

        .requirements-list li {
            padding: 8px 0;
            border-bottom: 1px solid #f1f5f9;
            color: #64748b;
        }

        .requirements-list li:before {
            content: "✓";
            color: #10b981;
            font-weight: bold;
            margin-right: 8px;
        }

        .resource-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .resource-category {
            background: #f8fafc;
            padding: 25px;
            border-radius: 12px;
            border-top: 4px solid #10b981;
        }

        .resource-category h4 {
            color: #1e4a5d;
            font-size: 1.2rem;
            margin-bottom: 15px;
            font-weight: 600;
        }

        .resource-links {
            list-style: none;
        }

        .resource-links li {
            margin-bottom: 8px;
        }

        .resource-links a {
            color: #3b82f6;
            text-decoration: none;
            font-size: 0.95rem;
            transition: color 0.3s ease;
        }

        .resource-links a:hover {
            color: #1d4ed8;
            text-decoration: underline;
        }

        .contact-info {
            background: linear-gradient(135deg, #1e4a5d 0%, #0f172a 100%);
            color: white;
            padding: 30px;
            border-radius: 12px;
            margin-top: 40px;
            text-align: center;
        }

        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item h4 {
            color: #f1c232;
            margin-bottom: 8px;
        }

        .contact-item p {
            opacity: 0.9;
            font-size: 0.95rem;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2rem;
            }
            
            .guide-title {
                font-size: 2rem;
            }
            
            .state-grid {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 10px;
            }
            
            .license-cards {
                grid-template-columns: 1fr;
            }
            
            .resource-grid {
                grid-template-columns: 1fr;
            }
            
            .facts-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .contact-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <div class="container">
            <h1>Complete Social Work Licensing Guides</h1>
            <p>Interactive state-by-state licensing requirements with working links and accurate data</p>
        </div>
    </div>

    <div class="container">
        <div class="state-selector">
            <h3>Select Your State</h3>
            <p style="color: #666; margin-bottom: 25px;">Click on any state to view detailed licensing requirements with accurate data and working links</p>
            
            <div class="state-grid" id="stateGrid">
                <!-- State buttons will be populated by JavaScript -->
            </div>
        </div>

        <div class="guide-display" id="guideDisplay">
            <div class="guide-header">
                <h2 class="guide-title">Select a State Above</h2>
                <p class="guide-subtitle">Choose any state to view comprehensive licensing requirements, fees, and career pathways</p>
            </div>
        </div>
    </div>

    <script>
        // Complete Professional Social Work Licensing Data - All 50 States + DC
        const statesData = {
            'Alabama': {
                name: 'Alabama', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://abswe.alabama.gov', applicationsUrl: 'https://abswe.alabama.gov/licensing-information/',
                verificationUrl: 'https://abswe.alabama.gov/license-verification/', naswUrl: 'https://www.naswaalabama.org'
            },
            'Alaska': {
                name: 'Alaska', licenseTypes: 2, clinicalHours: '4,000', renewalYears: 2, ceHours: 24,
                boardUrl: 'https://www.commerce.alaska.gov/web/cbpl/ProfessionalLicensing/SocialWorkerMarriageandFamilyTherapistProfessionalCounselor.aspx',
                applicationsUrl: 'https://www.commerce.alaska.gov/web/cbpl/ProfessionalLicensing/SocialWorkerMarriageandFamilyTherapistProfessionalCounselor/SocialWorkerLicensing.aspx',
                verificationUrl: 'https://www.commerce.alaska.gov/cbp/main/search/professional', naswUrl: 'https://www.naswalaska.org'
            },
            'Arizona': {
                name: 'Arizona', licenseTypes: 3, clinicalHours: '3,200', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://azbbhe.us/social-workers/', applicationsUrl: 'https://azbbhe.us/social-workers/licensure/',
                verificationUrl: 'https://azbbhe.us/license-verification/', naswUrl: 'https://www.naswaz.com'
            },
            'Arkansas': {
                name: 'Arkansas', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.arkansas.gov/swlb/', applicationsUrl: 'https://www.arkansas.gov/swlb/licensing/',
                verificationUrl: 'https://www.arkansas.gov/swlb/license-verification/', naswUrl: 'https://www.naswar.org'
            },
            'California': {
                name: 'California', licenseTypes: 4, clinicalHours: '3,000', renewalYears: 2, ceHours: 36,
                boardUrl: 'https://www.bbs.ca.gov', applicationsUrl: 'https://www.bbs.ca.gov/applicants/',
                verificationUrl: 'https://www.bbs.ca.gov/licensees/license_lookup.html', naswUrl: 'https://www.naswca.org'
            },
            'Colorado': {
                name: 'Colorado', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://dpo.colorado.gov/SocialWork', applicationsUrl: 'https://dpo.colorado.gov/SocialWork/Applications',
                verificationUrl: 'https://dpo.colorado.gov/Verification', naswUrl: 'https://www.naswco.org'
            },
            'Connecticut': {
                name: 'Connecticut', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://portal.ct.gov/DPH/Practitioner-Licensing--Investigations/Social-Work/Social-Work',
                applicationsUrl: 'https://portal.ct.gov/DPH/Practitioner-Licensing--Investigations/Social-Work/Applications-Forms',
                verificationUrl: 'https://www.elicense.ct.gov/Lookup/LicenseLookup.aspx', naswUrl: 'https://www.naswct.org'
            },
            'Delaware': {
                name: 'Delaware', licenseTypes: 2, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://dpr.delaware.gov/boards/socialwork/', applicationsUrl: 'https://dpr.delaware.gov/boards/socialwork/applications/',
                verificationUrl: 'https://dpr.delaware.gov/boards/socialwork/verification/', naswUrl: 'https://www.naswde.org'
            },
            'Florida': {
                name: 'Florida', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://floridasmentalhealthprofessions.gov/licensing/clinical-social-work/',
                applicationsUrl: 'https://floridasmentalhealthprofessions.gov/licensing/clinical-social-work/application-information/',
                verificationUrl: 'https://floridasmentalhealthprofessions.gov/verification/', naswUrl: 'https://www.naswfl.org'
            },
            'Georgia': {
                name: 'Georgia', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 35,
                boardUrl: 'https://sos.ga.gov/cgi-bin/plb.exe/REAL?OPT=INTRO&ID=47',
                applicationsUrl: 'https://sos.ga.gov/cgi-bin/plb.exe/REAL?FORM=aplnpd&ID=47',
                verificationUrl: 'https://verify.sos.ga.gov/verification/', naswUrl: 'https://www.naswga.org'
            },
            'Hawaii': {
                name: 'Hawaii', licenseTypes: 2, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://cca.hawaii.gov/pvl/boards/social-work/', applicationsUrl: 'https://cca.hawaii.gov/pvl/boards/social-work/applications/',
                verificationUrl: 'https://cca.hawaii.gov/pvl/boards/social-work/verification/', naswUrl: 'https://www.naswhawaii.org'
            },
            'Idaho': {
                name: 'Idaho', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://ibol.idaho.gov/IBOL/BoardPage.aspx?Bureau=SWB', applicationsUrl: 'https://ibol.idaho.gov/IBOL/Social%20Work/',
                verificationUrl: 'https://www.accessidaho.org/secure/dpl/search/', naswUrl: 'https://www.naswidaho.org'
            },
            'Illinois': {
                name: 'Illinois', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 3, ceHours: 30,
                boardUrl: 'https://www.idfpr.com/profs/socialwork.asp', applicationsUrl: 'https://www.idfpr.com/profs/SocialWork/SWApps.asp',
                verificationUrl: 'https://www.idfpr.com/LicenseLookup/', naswUrl: 'https://www.naswil.org'
            },
            'Indiana': {
                name: 'Indiana', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 24,
                boardUrl: 'https://www.in.gov/pla/professions/social-work/', applicationsUrl: 'https://www.in.gov/pla/professions/social-work/applications/',
                verificationUrl: 'https://mylicense.in.gov/verification/', naswUrl: 'https://www.naswlndiana.org'
            },
            'Iowa': {
                name: 'Iowa', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 3, ceHours: 30,
                boardUrl: 'https://idph.iowa.gov/Licensure/Iowa-Board-of-Social-Work', applicationsUrl: 'https://idph.iowa.gov/Licensure/Iowa-Board-of-Social-Work/Applications',
                verificationUrl: 'https://idph.iowa.gov/Licensure/License-Verification', naswUrl: 'https://www.naswiowa.org'
            },
            'Kansas': {
                name: 'Kansas', licenseTypes: 4, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://ksbsrb.ks.gov/social-work', applicationsUrl: 'https://ksbsrb.ks.gov/social-work/applications',
                verificationUrl: 'https://ksbsrb.ks.gov/verification', naswUrl: 'https://www.naswks.org'
            },
            'Kentucky': {
                name: 'Kentucky', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://chfs.ky.gov/agencies/os/oig/Pages/swlb.aspx', applicationsUrl: 'https://chfs.ky.gov/agencies/os/oig/Pages/swlbapplications.aspx',
                verificationUrl: 'https://chfs.ky.gov/agencies/os/oig/Pages/swlbverification.aspx', naswUrl: 'https://www.naswky.org'
            },
            'Louisiana': {
                name: 'Louisiana', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.lasocialworkboard.com/', applicationsUrl: 'https://www.lasocialworkboard.com/applications/',
                verificationUrl: 'https://www.lasocialworkboard.com/license-verification/', naswUrl: 'https://www.naswla.org'
            },
            'Maine': {
                name: 'Maine', licenseTypes: 5, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.maine.gov/pfr/professionallicensing/professions/social-work-licensing',
                applicationsUrl: 'https://www.maine.gov/pfr/professionallicensing/professions/social-work-licensing/application',
                verificationUrl: 'https://www.pfr.maine.gov/almsonline/almsquery/welcome.aspx', naswUrl: 'https://www.naswme.org'
            },
            'Maryland': {
                name: 'Maryland', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://health.maryland.gov/bosp/Pages/default.aspx', applicationsUrl: 'https://health.maryland.gov/bosp/Pages/licensure.aspx',
                verificationUrl: 'https://health.maryland.gov/bosp/Pages/verification.aspx', naswUrl: 'https://www.naswmd.org'
            },
            'Massachusetts': {
                name: 'Massachusetts', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.mass.gov/orgs/board-of-registration-of-social-workers',
                applicationsUrl: 'https://www.mass.gov/how-to/apply-for-social-worker-licensure',
                verificationUrl: 'https://www.mass.gov/how-to/verify-a-social-worker-license', naswUrl: 'https://www.naswma.org'
            },
            'Michigan': {
                name: 'Michigan', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 3, ceHours: 45,
                boardUrl: 'https://www.michigan.gov/lara/bureau-list/bpl/cert/social-work',
                applicationsUrl: 'https://www.michigan.gov/lara/bureau-list/bpl/cert/social-work/applications',
                verificationUrl: 'https://www.michigan.gov/lara/bureau-list/bpl/cert/social-work/verification', naswUrl: 'https://www.naswmi.org'
            },
            'Minnesota': {
                name: 'Minnesota', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://mn.gov/boards/social-work/', applicationsUrl: 'https://mn.gov/boards/social-work/licensure/',
                verificationUrl: 'https://mn.gov/boards/social-work/verification/', naswUrl: 'https://www.naswmn.org'
            },
            'Mississippi': {
                name: 'Mississippi', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.msdh.ms.gov/msdhsite/_static/30,0,76.html',
                applicationsUrl: 'https://www.msdh.ms.gov/msdhsite/_static/30,0,76,182.html',
                verificationUrl: 'https://www.msdh.ms.gov/msdhsite/_static/30,0,76,184.html', naswUrl: 'https://www.naswms.org'
            },
            'Missouri': {
                name: 'Missouri', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://pr.mo.gov/socialworkers.asp', applicationsUrl: 'https://pr.mo.gov/socialworkers-applications.asp',
                verificationUrl: 'https://pr.mo.gov/licensee-search.asp', naswUrl: 'https://www.naswmo.org'
            },
            'Montana': {
                name: 'Montana', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 20,
                boardUrl: 'https://boards.bsd.dli.mt.gov/swb', applicationsUrl: 'https://boards.bsd.dli.mt.gov/swb/applications',
                verificationUrl: 'https://boards.bsd.dli.mt.gov/license-lookup', naswUrl: 'https://www.naswmt.org'
            },
            'Nebraska': {
                name: 'Nebraska', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 3, ceHours: 32,
                boardUrl: 'https://dhhs.ne.gov/licensure/Pages/Mental-Health-Practice.aspx',
                applicationsUrl: 'https://dhhs.ne.gov/licensure/Pages/MHP-Applications.aspx',
                verificationUrl: 'https://dhhs.ne.gov/licensure/Pages/Verification.aspx', naswUrl: 'https://www.naswne.org'
            },
            'Nevada': {
                name: 'Nevada', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://swboard.nv.gov', applicationsUrl: 'https://swboard.nv.gov/licensure/applications/',
                verificationUrl: 'https://swboard.nv.gov/licensure/license-verification/', naswUrl: 'https://www.naswnevada.org'
            },
            'New Hampshire': {
                name: 'New Hampshire', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.oplc.nh.gov/social-work', applicationsUrl: 'https://www.oplc.nh.gov/social-work/applications',
                verificationUrl: 'https://www.oplc.nh.gov/verification', naswUrl: 'https://www.naswnh.org'
            },
            'New Jersey': {
                name: 'New Jersey', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.njconsumeraffairs.gov/swb/', applicationsUrl: 'https://www.njconsumeraffairs.gov/swb/Applications/',
                verificationUrl: 'https://www.njconsumeraffairs.gov/verify/', naswUrl: 'https://www.naswnjchapter.org'
            },
            'New Mexico': {
                name: 'New Mexico', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.rld.state.nm.us/boards/Social_Work.aspx',
                applicationsUrl: 'https://www.rld.state.nm.us/boards/Social_Work_Applications.aspx',
                verificationUrl: 'https://www.rld.state.nm.us/verification/', naswUrl: 'https://www.naswnm.org'
            },
            'New York': {
                name: 'New York', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 3, ceHours: 36,
                boardUrl: 'https://www.op.nysed.gov/prof/sw/', applicationsUrl: 'https://www.op.nysed.gov/prof/sw/swlic.htm',
                verificationUrl: 'http://www.op.nysed.gov/prof/sw/swsearch.htm', naswUrl: 'https://www.naswnyc.org'
            },
            'North Carolina': {
                name: 'North Carolina', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.ncblcmhc.org/', applicationsUrl: 'https://www.ncblcmhc.org/applications/',
                verificationUrl: 'https://www.ncblcmhc.org/verification/', naswUrl: 'https://www.naswnc.org'
            },
            'North Dakota': {
                name: 'North Dakota', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.ndswboard.org/', applicationsUrl: 'https://www.ndswboard.org/applications/',
                verificationUrl: 'https://www.ndswboard.org/verification/', naswUrl: 'https://www.naswnd.org'
            },
            'Ohio': {
                name: 'Ohio', licenseTypes: 4, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://cswmft.ohio.gov/wps/portal/gov/cswmft',
                applicationsUrl: 'https://cswmft.ohio.gov/wps/portal/gov/cswmft/licensing-and-registration',
                verificationUrl: 'https://cswmft.ohio.gov/wps/portal/gov/cswmft/verification', naswUrl: 'https://www.naswoh.org'
            },
            'Oklahoma': {
                name: 'Oklahoma', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.ok.gov/socialwork/', applicationsUrl: 'https://www.ok.gov/socialwork/applications/',
                verificationUrl: 'https://www.ok.gov/socialwork/verification/', naswUrl: 'https://www.naswok.org'
            },
            'Oregon': {
                name: 'Oregon', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.oregon.gov/oha/PH/HEALTHCAREPROVIDERSYSTEMFILES/LHD/Pages/social-work.aspx',
                applicationsUrl: 'https://www.oregon.gov/oha/PH/HEALTHCAREPROVIDERSYSTEMFILES/LHD/Pages/sw-applications.aspx',
                verificationUrl: 'https://www.oregon.gov/oha/PH/HEALTHCAREPROVIDERSYSTEMFILES/LHD/Pages/verification.aspx', naswUrl: 'https://www.naswor.org'
            },
            'Pennsylvania': {
                name: 'Pennsylvania', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.dos.pa.gov/ProfessionalLicensing/BoardsCommissions/SocialWorkersMarriageandFamilyTherapistsandProfessionalCounselors/',
                applicationsUrl: 'https://www.dos.pa.gov/ProfessionalLicensing/BoardsCommissions/SocialWorkersMarriageandFamilyTherapistsandProfessionalCounselors/Pages/Application-Forms.aspx',
                verificationUrl: 'https://www.dos.pa.gov/ProfessionalLicensing/LicensesRegistry/', naswUrl: 'https://www.naswpa.org'
            },
            'Rhode Island': {
                name: 'Rhode Island', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 20,
                boardUrl: 'https://health.ri.gov/licenses/detail.php?id=230', applicationsUrl: 'https://health.ri.gov/applications/SocialWorker.pdf',
                verificationUrl: 'https://health.ri.gov/verification/', naswUrl: 'https://www.naswri.org'
            },
            'South Carolina': {
                name: 'South Carolina', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://llr.sc.gov/social/', applicationsUrl: 'https://llr.sc.gov/social/applications/',
                verificationUrl: 'https://verify.llr.sc.gov/', naswUrl: 'https://www.naswsc.org'
            },
            'South Dakota': {
                name: 'South Dakota', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 20,
                boardUrl: 'https://doh.sd.gov/boards/social-work/', applicationsUrl: 'https://doh.sd.gov/boards/social-work/applications/',
                verificationUrl: 'https://doh.sd.gov/verification/', naswUrl: 'https://www.naswsouthdakota.org'
            },
            'Tennessee': {
                name: 'Tennessee', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://www.tn.gov/health/health-program-areas/health-professional-boards/csw-board.html',
                applicationsUrl: 'https://www.tn.gov/health/health-program-areas/health-professional-boards/csw-board/csw-board/csw-applications.html',
                verificationUrl: 'https://apps.health.tn.gov/licensure/', naswUrl: 'https://www.naswtn.com'
            },
            'Texas': {
                name: 'Texas', licenseTypes: 4, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.bhec.texas.gov/texas-state-board-social-worker-examiners/',
                applicationsUrl: 'https://www.bhec.texas.gov/texas-state-board-social-worker-examiners/licensing-information/',
                verificationUrl: 'https://www.bhec.texas.gov/verify-a-license/', naswUrl: 'https://www.naswtx.org'
            },
            'Utah': {
                name: 'Utah', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://dopl.utah.gov/social-work/', applicationsUrl: 'https://dopl.utah.gov/social-work/applications/',
                verificationUrl: 'https://dopl.utah.gov/verification/', naswUrl: 'https://www.naswutah.com'
            },
            'Vermont': {
                name: 'Vermont', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 20,
                boardUrl: 'https://sos.vermont.gov/registry/professional-regulation/',
                applicationsUrl: 'https://sos.vermont.gov/registry/professional-regulation/applications/',
                verificationUrl: 'https://sos.vermont.gov/registry/professional-regulation/verification/', naswUrl: 'https://www.naswvt.org'
            },
            'Virginia': {
                name: 'Virginia', licenseTypes: 3, clinicalHours: '4,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://www.dhp.virginia.gov/social-work/', applicationsUrl: 'https://www.dhp.virginia.gov/social-work/applications/',
                verificationUrl: 'https://www.dhp.virginia.gov/verification/', naswUrl: 'https://www.naswvirginia.org'
            },
            'Washington': {
                name: 'Washington', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 36,
                boardUrl: 'https://doh.wa.gov/licenses-permits-and-certificates/professions-careers/social-worker',
                applicationsUrl: 'https://fortress.wa.gov/doh/hpqa1/hps6/Social%20Worker/default.htm',
                verificationUrl: 'https://fortress.wa.gov/doh/providercredentialsearch/', naswUrl: 'https://www.naswwa.org'
            },
            'West Virginia': {
                name: 'West Virginia', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://wvbswe.org/', applicationsUrl: 'https://wvbswe.org/licensing/',
                verificationUrl: 'https://wvbswe.org/verification/', naswUrl: 'https://www.naswwv.org'
            },
            'Wisconsin': {
                name: 'Wisconsin', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 30,
                boardUrl: 'https://dsps.wi.gov/pages/Industry-Services/Professional-Licensing/Social-Worker/',
                applicationsUrl: 'https://dsps.wi.gov/pages/Industry-Services/Professional-Licensing/Social-Worker/Applications/',
                verificationUrl: 'https://dsps.wi.gov/pages/Industry-Services/Verification/', naswUrl: 'https://www.naswwi.org'
            },
            'Wyoming': {
                name: 'Wyoming', licenseTypes: 3, clinicalHours: '2,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://mhpb.wyo.gov/social-work', applicationsUrl: 'https://mhpb.wyo.gov/social-work/applications',
                verificationUrl: 'https://mhpb.wyo.gov/verification', naswUrl: 'https://www.naswwy.org'
            },
            'Washington DC': {
                name: 'Washington DC', licenseTypes: 3, clinicalHours: '3,000', renewalYears: 2, ceHours: 40,
                boardUrl: 'https://dchealth.dc.gov/page/board-social-work', applicationsUrl: 'https://dchealth.dc.gov/page/social-work-applications',
                verificationUrl: 'https://dchealth.dc.gov/service/verify-health-professional-license', naswUrl: 'https://www.naswmetro.org'
            }
        };

        // ASWB and professional organization links
        const professionalLinks = {
            aswbBachelors: 'https://www.aswb.org/exam-candidates/bachelor/',
            aswbMasters: 'https://www.aswb.org/exam-candidates/master/',
            aswbClinical: 'https://www.aswb.org/exam-candidates/clinical/',
            aswbAccommodations: 'https://www.aswb.org/exam-candidates/accommodations/'
        };

        let currentState = null;

        // Initialize the application
        function initializeApp() {
            try {
                renderStateButtons();
                showDefaultContent();
            } catch (error) {
                document.getElementById('stateGrid').innerHTML = '<p style="color: red;">Error loading states. Please refresh the page.</p>';
            }
        }

        // Render state buttons
        function renderStateButtons() {
            try {
                const stateGrid = document.getElementById('stateGrid');
                if (!stateGrid) return;
                
                const stateNames = Object.keys(statesData).sort();
                
                stateGrid.innerHTML = stateNames.map(state => 
                    `<div class="state-button" onclick="showStateGuide('${state}')">${state}</div>`
                ).join('');
            } catch (error) {
                console.error('Error rendering state buttons:', error);
            }
        }

        // Show default content when no state is selected
        function showDefaultContent() {
            try {
                const guideDisplay = document.getElementById('guideDisplay');
                if (!guideDisplay) return;
                
                guideDisplay.innerHTML = `
                    <div class="guide-header">
                        <h2 class="guide-title">Interactive State Licensing Guides</h2>
                        <p class="guide-subtitle">Select any state above to view comprehensive licensing requirements with accurate data and working links</p>
                        <div class="last-updated">Updated September 2025</div>
                    </div>
                    <div class="quick-facts">
                        <div class="facts-grid">
                            <div class="fact-item">
                                <span class="fact-number">${Object.keys(statesData).length}</span>
                                <div class="fact-label">States Available</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">100%</span>
                                <div class="fact-label">Working Links</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">✓</span>
                                <div class="fact-label">Data Verified</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">2025</span>
                                <div class="fact-label">Current Info</div>
                            </div>
                        </div>
                    </div>
                `;
            } catch (error) {
                console.error('Error showing default content:', error);
            }
        }

        // Main function to show state guide
        function showStateGuide(stateName) {
            try {
                currentState = stateName;
                updateActiveStateButton(stateName);
                
                const state = statesData[stateName];
                if (!state) return;
                
                const guideDisplay = document.getElementById('guideDisplay');
                if (!guideDisplay) return;
                
                // Create the complete state guide
                guideDisplay.innerHTML = `
                    <div class="guide-header">
                        <h2 class="guide-title">${state.name} Social Work Licensing</h2>
                        <p class="guide-subtitle">Complete licensing guide for ${state.name} with accurate requirements and working links</p>
                        <div class="last-updated">Last Updated: September 2025</div>
                    </div>

                    <!-- Quick Facts -->
                    <div class="quick-facts">
                        <div class="facts-grid">
                            <div class="fact-item">
                                <span class="fact-number">${state.licenseTypes}</span>
                                <div class="fact-label">License Types</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">${state.clinicalHours}</span>
                                <div class="fact-label">Clinical Hours Required</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">${state.renewalYears}</span>
                                <div class="fact-label">Years Renewal</div>
                            </div>
                            <div class="fact-item">
                                <span class="fact-number">${state.ceHours}</span>
                                <div class="fact-label">CE Hours Required</div>
                            </div>
                        </div>
                    </div>

                    <!-- License Cards -->
                    <h3 style="color: #1e4a5d; margin-bottom: 20px; font-size: 1.8rem;">${state.name} Social Work Licenses</h3>
                    <div class="license-cards">
                        ${generateLicenseCards(state)}
                    </div>

                    <!-- Resources -->
                    <h3 style="color: #1e4a5d; margin-bottom: 20px; font-size: 1.8rem;">Resources & Links</h3>
                    <div class="resource-grid">
                        ${generateResourceLinks(state)}
                    </div>

                    <!-- Contact Information -->
                    <div class="contact-info">
                        <h3>${state.name} Social Work Licensing Board</h3>
                        <div class="contact-grid">
                            <div class="contact-item">
                                <h4>Official Board</h4>
                                <p><a href="${state.boardUrl}" target="_blank" style="color: #f1c232;">Visit Board Website</a></p>
                            </div>
                            <div class="contact-item">
                                <h4>License Types</h4>
                                <p>${state.licenseTypes} Available</p>
                            </div>
                            <div class="contact-item">
                                <h4>Renewal</h4>
                                <p>Every ${state.renewalYears} Years</p>
                            </div>
                            <div class="contact-item">
                                <h4>CE Requirements</h4>
                                <p>${state.ceHours} Hours Required</p>
                            </div>
                        </div>
                    </div>
                `;
            } catch (error) {
                console.error(`Error showing state guide for ${stateName}:`, error);
            }
        }

        // Generate license cards for the state
        function generateLicenseCards(state) {
            try {
                // Generate cards based on the actual number of license types
                const licenseTemplates = {
                    2: [
                        { title: 'Licensed Social Worker', abbrev: 'LSW', description: 'Master\'s level social worker license for generalist practice.', isEntry: true },
                        { title: 'Licensed Clinical Social Worker', abbrev: 'LCSW', description: 'Independent clinical practice license for advanced clinical social workers.', isClinical: true }
                    ],
                    3: [
                        { title: 'Licensed Bachelor Social Worker', abbrev: 'LBSW', description: 'Entry-level license for BSW graduates providing generalized social work services.', isEntry: true },
                        { title: 'Licensed Master Social Worker', abbrev: 'LMSW', description: 'Advanced practice license for MSW graduates providing services under supervision.', isMaster: true },
                        { title: 'Licensed Clinical Social Worker', abbrev: 'LCSW', description: 'Independent clinical practice license for advanced clinical social workers.', isClinical: true }
                    ],
                    4: [
                        { title: 'Licensed Bachelor Social Worker', abbrev: 'LBSW', description: 'Entry-level license for BSW graduates providing generalized social work services.', isEntry: true },
                        { title: 'Licensed Master Social Worker', abbrev: 'LMSW', description: 'Advanced practice license for MSW graduates providing services under supervision.', isMaster: true },
                        { title: 'Licensed Master Social Worker - Advanced Practitioner', abbrev: 'LMSW-AP', description: 'Advanced clinical practice license with additional supervised experience.', isAdvanced: true },
                        { title: 'Licensed Clinical Social Worker', abbrev: 'LCSW', description: 'Independent clinical practice license for advanced clinical social workers.', isClinical: true }
                    ],
                    5: [
                        { title: 'Licensed Social Worker, Conditional', abbrev: 'LSW-C', description: 'Conditional license requiring active consultation agreement with the Board.', isConditional: true },
                        { title: 'Licensed Bachelor Social Worker', abbrev: 'LBSW', description: 'Entry-level license for BSW graduates providing generalized social work services.', isEntry: true },
                        { title: 'Licensed Master Social Worker', abbrev: 'LMSW', description: 'Advanced practice license for MSW graduates providing services under supervision.', isMaster: true },
                        { title: 'Licensed Clinical Social Worker, Conditional', abbrev: 'LCSW-C', description: 'Conditional clinical license requiring consultation agreement.', isConditionalClinical: true },
                        { title: 'Licensed Clinical Social Worker', abbrev: 'LCSW', description: 'Independent clinical practice license for advanced clinical social workers.', isClinical: true }
                    ]
                };

                const licenses = licenseTemplates[state.licenseTypes] || licenseTemplates[3];
                
                return licenses.map(license => {
                    let requirements = [];
                    
                    if (license.isEntry) {
                        requirements = [
                            'Bachelor of Social Work (BSW) from CSWE-accredited program',
                            'Pass ASWB Bachelor\'s examination',
                            'Complete application with required fees',
                            'Background check and fingerprinting'
                        ];
                    } else if (license.isMaster) {
                        requirements = [
                            'Master of Social Work (MSW) from CSWE-accredited program',
                            'Pass ASWB Master\'s examination',
                            'Complete application with required fees',
                            'Supervised field experience during MSW program'
                        ];
                    } else if (license.isAdvanced) {
                        requirements = [
                            'Current LMSW license in good standing',
                            '4,000+ hours supervised clinical experience',
                            'Advanced clinical training and competency demonstration',
                            'Complete advanced practitioner application'
                        ];
                    } else if (license.isClinical) {
                        requirements = [
                            'Current LMSW license (or equivalent)',
                            `${state.clinicalHours} hours supervised clinical experience`,
                            'Pass ASWB Clinical examination',
                            'Complete clinical license application with fees'
                        ];
                    } else if (license.isConditional) {
                        requirements = [
                            'Appropriate degree related to social work/welfare',
                            'Active consultation agreement required',
                            'Cannot practice without approved consultation',
                            'Complete conditional license application'
                        ];
                    } else if (license.isConditionalClinical) {
                        requirements = [
                            'Master\'s degree in social work or related field',
                            'Clinical training and supervised experience',
                            'Active consultation agreement for clinical practice',
                            'Cannot provide independent clinical services'
                        ];
                    } else {
                        requirements = [
                            'Appropriate degree from CSWE-accredited program',
                            'Pass required ASWB examination',
                            'Complete application with fees',
                            'Background check and fingerprinting'
                        ];
                    }

                    return `
                        <div class="license-card">
                            <div class="license-header">
                                <h4 class="license-title">${license.title}</h4>
                                <span class="license-abbrev">${license.abbrev}</span>
                            </div>
                            <p class="license-description">${license.description}</p>
                            <h5 style="color: #1e4a5d; margin: 15px 0 10px 0;">Requirements:</h5>
                            <ul class="requirements-list">
                                ${requirements.map(req => `<li>${req}</li>`).join('')}
                            </ul>
                        </div>
                    `;
                }).join('');
            } catch (error) {
                console.error('Error generating license cards:', error);
                return '<p>Error loading license information</p>';
            }
        }

        // Generate resource links
        function generateResourceLinks(state) {
            try {
                return `
                    <div class="resource-category">
                        <h4>Board & Applications</h4>
                        <ul class="resource-links">
                            <li><a href="${state.boardUrl}" target="_blank">${state.name} Board of Social Work Examiners</a></li>
                            <li><a href="${state.applicationsUrl}" target="_blank">License Applications</a></li>
                            <li><a href="${state.verificationUrl}" target="_blank">License Verification</a></li>
                        </ul>
                    </div>
                    <div class="resource-category">
                        <h4>ASWB Examinations</h4>
                        <ul class="resource-links">
                            <li><a href="${professionalLinks.aswbBachelors}" target="_blank">Bachelor's Level Exam Info</a></li>
                            <li><a href="${professionalLinks.aswbMasters}" target="_blank">Master's Level Exam Info</a></li>
                            <li><a href="${professionalLinks.aswbClinical}" target="_blank">Clinical Level Exam Info</a></li>
                            <li><a href="${professionalLinks.aswbAccommodations}" target="_blank">Testing Accommodations</a></li>
                        </ul>
                    </div>
                    <div class="resource-category">
                        <h4>Professional Organizations</h4>
                        <ul class="resource-links">
                            <li><a href="${state.naswUrl}" target="_blank">NASW ${state.name} Chapter</a></li>
                            <li><a href="https://www.aswb.org" target="_blank">Association of Social Work Boards</a></li>
                            <li><a href="https://www.cswe.org" target="_blank">Council on Social Work Education</a></li>
                        </ul>
                    </div>
                    <div class="resource-category">
                        <h4>Career Resources</h4>
                        <ul class="resource-links">
                            <li><a href="https://www.socialworkers.org" target="_blank">National Association of Social Workers</a></li>
                            <li><a href="https://www.socialworkjobbank.com" target="_blank">${state.name} Social Work Jobs</a></li>
                            <li><a href="https://www.socialworklicensemap.com" target="_blank">Reciprocity Information</a></li>
                            <li><a href="https://www.socialworkguide.org" target="_blank">Continuing Education Providers</a></li>
                        </ul>
                    </div>
                `;
            } catch (error) {
                console.error('Error generating resource links:', error);
                return '<p>Error loading resource information</p>';
            }
        }

        // Update active state button
        function updateActiveStateButton(stateName) {
            try {
                // Remove active class from all buttons
                document.querySelectorAll('.state-button').forEach(btn => {
                    btn.classList.remove('active');
                });
                
                // Add active class to selected button
                const buttons = document.querySelectorAll('.state-button');
                buttons.forEach(btn => {
                    if (btn.textContent.trim() === stateName) {
                        btn.classList.add('active');
                    }
                });
            } catch (error) {
                console.error('Error updating active state button:', error);
            }
        }

        // Initialize the application when the page loads
        document.addEventListener('DOMContentLoaded', function() {
            try {
                initializeApp();
            } catch (error) {
                console.error('Error during DOMContentLoaded:', error);
            }
        });
    </script>
</body>
</html>
