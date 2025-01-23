<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>User Tools</title>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Orbitron', sans-serif;
            margin: 0;
            padding: 0;
            background: #1a1a1a; /* Dark background */
            color: #e0e0e0; /* Light text color for contrast */
        }
        header {
            background: linear-gradient(45deg, #2e2e2e, #383838); /* Sleek dark gradient */
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.6);
        }
        h1 {
            font-size: 2rem;
            color: #fff;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.4);
        }
        nav {
            display: flex;
            gap: 1.5rem;
        }
        nav .dropdown {
            position: relative;
        }
        nav .dropdown > a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            cursor: pointer;
            text-transform: uppercase;
            font-size: 1.1rem;
            letter-spacing: 1px;
            transition: color 0.3s ease;
        }
        nav .dropdown-content {
            display: none;
            position: absolute;
            background: rgba(0, 0, 0, 0.8);
            padding: 0.5rem 0;
            border-radius: 5px;
            top: 100%;
            left: 0;
            min-width: 150px;
            z-index: 1001;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.6);
        }
        nav .dropdown-content a {
            display: block;
            padding: 0.5rem 1rem;
            color: #00bcd4; /* Cyan for cool accent */
            text-decoration: none;
            font-weight: normal;
            font-size: 1rem;
            transition: background 0.3s, color 0.3s;
        }
        nav .dropdown-content a:hover {
            background: #00bcd4;
            color: black; /* Inverted colors for hover */
        }
        nav .dropdown:hover .dropdown-content {
            display: block;
        }
        main {
            padding: 2rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        .tool {
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.5); /* Dark transparent background */
            backdrop-filter: blur(15px);
            padding: 1.5rem;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.7);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .tool:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0, 188, 212, 0.7); /* Cyan glow on hover */
        }
        .tool h2 {
            margin: 0;
            font-size: 1.8rem;
            color: #00bcd4; /* Cyan for cool effect */
            text-shadow: 0 0 15px rgba(0, 188, 212, 0.5);
        }
        .tool p {
            margin: 0.5rem 0 0;
            line-height: 1.5;
            color: #b3b3b3; /* Light grey text */
        }
        footer {
            background: linear-gradient(45deg, #2e2e2e, #383838); /* Same dark gradient as header */
            color: white;
            text-align: center;
            padding: 1.5rem;
            position: fixed;
            bottom: 0;
            width: 100%;
            box-shadow: 0 -4px 15px rgba(0, 0, 0, 0.6);
        }
        footer p {
            font-size: 1rem;
            text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
        }
    </style>
</head>
<body>
    <header>
        <h1>QB User Tools</h1>
        <nav>
            <div class="dropdown">
                <a href="#">Floor Information</a>
                <div class="dropdown-content">
                    <a href="https://prod-na.manage.robotics.amazon.dev" target="_blank">Optic Manager</a>
					<a href="https://na.prod.command-center.robotics.amazon.dev/SAT1/mod/A" target="_blank">QBCC</a>
					<a href="https://atlas-kibana.corp.amazon.com/app/kibana#/dashboard/4d1cf850-4517-11ea-9a86-43221f1fe5b0?_g=(refreshInterval:(display:Off,pause:!f,value:0),time:(from:'2025-01-15T00:00:00.000Z',mode:absolute,to:'2025-01-15T10:30:00.000Z'))&_a=(description:'SAT1%20Amnesty%20Dashboard%20Created%2002%2F2020',filters:!(('$state':(store:appState),meta:(alias:!n,disabled:!f,index:'216dae00-3af7-11e9-96e0-8d1f738315f8',key:warehouse_id,negate:!f,params:(query:SAT1,type:phrase),type:phrase,value:SAT1),query:(match:(warehouse_id:(query:SAT1,type:phrase))))),fullScreenMode:!f,options:(darkTheme:!t,hidePanelTitles:!f,useMargins:!t),panels:!((embeddableConfig:(vis:(colors:(Count:%23806EB7),legendOpen:!t)),gridData:(h:9,i:'1',w:36,x:0,y:0),id:c956c970-4502-11e9-86f1-a72adc4935ed,panelIndex:'1',type:visualization,version:'6.3.0'),(embeddableConfig:(vis:(colors:(Quantity:%23447EBC),legendOpen:!t)),gridData:(h:15,i:'3',w:16,x:0,y:24),id:'155ee5f0-4503-11e9-86f1-a72adc4935ed',panelIndex:'3',title:'ICQA%20APMT%20By%20User%20(Top%2010)',type:visualization,version:'6.3.0'),(embeddableConfig:(vis:(colors:(Quantity:%23447EBC),legendOpen:!t)),gridData:(h:15,i:'4',w:16,x:32,y:24),id:'1ba530e0-4503-11e9-a572-c3a1576aa62f',panelIndex:'4',title:'ICQA%20APMT%20By%20Manager%20(Top%2010)',type:visualization,version:'6.3.0'),(embeddableConfig:(spy:!n,vis:(colors:(P-0-B:%23AEA2E0,P-1-A:%23BADFF4,P-1-B:%23DEDAF7,P-1-F:%23B7DBAB,P-6-A:%239AC48A,P-7-A:%23806EB7,P-8-A:%23E0F9D7,paKivaA01:%23447EBC,paKivaA01G:%23447EBC,paKivaA02:%23806EB7,paKivaA03:%239AC48A,paKivaA04:%2382B5D8,paKivaB03:%2370DBED))),gridData:(h:15,i:'5',w:16,x:0,y:9),id:fb1354b0-4502-11e9-86f1-a72adc4935ed,panelIndex:'5',title:'ICQA%20APMT%20By%20Pick%20Area',type:visualization,version:'6.3.0'),(embeddableConfig:(vis:(colors:(Quantity:%239AC48A),legendOpen:!t)),gridData:(h:15,i:'7',w:16,x:16,y:9),id:'2c125c50-4503-11e9-8a46-bbf85c8a8a5d',panelIndex:'7',title:'ICQA%20APMT%20By%20Bin%20(Top%2010)',type:visualization,version:'6.3.0'),(embeddableConfig:(vis:(colors:(Quantity:%239AC48A),legendOpen:!t)),gridData:(h:15,i:'8',w:16,x:32,y:9),id:'23e4b3c0-4503-11e9-8a46-bbf85c8a8a5d" target="_blank">SAT1 Amnesty Dashboard - Kibana</a>
					<a href="https://www.example4.com" target="_blank">Optic Manager</a>
                    <a href="https://vantage.amazon.com/app/fulfillment-dashboards/floor-issue-overview?customer=AMZN&warehouse=SAT1&region=us-east-1&zones=paKivaA01%2CpaKivaA02" target="_blank">Vantage Floor Issue Overview</a>
                    <a href="https://roboscout-dub.corp.amazon.com/analyze/19899/?datasource_current_day=false&datasource_endDateTime=2025-01-11%2012:00:00&datasource_startDateTime=2025-01-11%2000:00:00&datasource_viz=nvd3Table&mom_ids=465%2C461&ofm_ids=&osm_ids=40&oxm_ids=285&sites=(SAT1-paKivaA01)(SAT1-paKivaA02)" target="_blank">Avg Responce Time</a>
                </div>
            </div>
            <div class="dropdown">
                <a href="#">Building Information</a>
                <div class="dropdown-content">
                    <a href="https://sera-na.amazon.com/SAT1?shiftId=895a8060-a5b3-421d-bcf9-7aaaf62202d7" target="_blank">Sera</a>
                    <a href="https://rodeo-iad.amazon.com/SAT1/ExSD?yAxis=PROCESS_PATH&zAxis=WORK_POOL&shipmentTypes=CUSTOMER_SHIPMENTS&_shipmentTypes=on&exSDRange.quickRange=NEXT_3_DAYS&exSDRange.dailyStart=00%3A00&exSDRange.dailyEnd=00%3A00&giftOption=ALL&fulfillmentServiceClass=ALL&fracs=NON_FRACS&workPool=ReadyToPick&workPool=PickingNotYetPicked&workPool=CrossdockNotYetPicked&_workPool=on&workPool=PickingPicked&workPool=Inducted&workPool=RebinBuffered&workPool=Sorted&workPool=GiftWrap&workPool=Packing&workPool=Scanned&workPool=ProblemSolving&workPool=ProcessPartial&workPool=SoftwareException&workPool=Crossdock&workPool=PreSort&workPool=TransshipSorted&workPool=Palletized&_workPool=on&_workPool=on&processPath=&shipMethod=&shipOption=&sortCode=&fnSku" target="_blank">Rodeo</a>
                </div>
            </div>
            <div class="dropdown">
                <a href="#">Problem Solve Tools</a>
                <div class="dropdown-content">
                    <a href="https://fcresearch-na.aka.amazon.com/SAT1/search" target="_blank">FC Research</a>
                    <a href="#" target="_blank">Add Item</a>
                    <a href="#" target="_blank">Edit Item</a>
                    <a href="#" target="_blank">Move Item</a>
                </div>
            </div>
			<div class="dropdown">
                <a href="#">Pod Tools</a>
                <div class="dropdown-content">
                    <a href="https://fccapacityconfiguration-na.amazon.com/fc/SAT1/bayUtilities/viewBay?locale=en_US" target="_blank">Bay Utilities</a>
                    <a href="https://fccapacityconfiguration-na.amazon.com/fc/SAT1/binUtilities/viewBin?locale=en_US" target="_blank">Bin Utilities</a>
                    <a href="https://ar-podmanager-iad.iad.proxy.amazon.com/" target="_blank">Pod Manager</a>
                </div>
            </div>
            <div class="dropdown">
                <a href="#">FCLM</a>
                <div class="dropdown-content">
                    <a href="https://fcmenu-iad-regionalized.corp.amazon.com/SAT1/laborTrackingKiosk" target="_blank">Labor Tracking</a>
                    <a href="https://fclm-portal.amazon.com/reports/timeOnTask?reportFormat=HTML&warehouseId=SAT1&maxIntradayDays=30&spanType=Intraday&startDateIntraday=2022%2F01%2F06&startHourIntraday=18&startMinuteIntraday=0&endDateIntraday=2022%2F01%2F07&endHourIntraday=6&endMinuteIntraday=0" target="_blank">Time on Task</a>
                </div>
            </div>
            <div class="dropdown">
                <a href="https://fcmenu-iad-regionalized.corp.amazon.com/SAT1" target="_blank">FC Menu</a>
            </div>
            <div class="dropdown">
                <a href="https://www.example5.com" target="_blank">Apollo</a>
            </div>
            <div class="dropdown">
                <a href="https://fc-count-scanner-tools-iad-jlb-l-iad.iad.proxy.amazon.com/app/amnesty-add-back" target="_blank">Amnesty AddBack</a>
            </div>
        </nav>
    </header>
    <main>
        <div id="floorinfo" class="tool">
            <h2>Floor Information</h2>
            <p>A tool to manage and view the floor information for better interaction.</p>
            <img src="https://assets.aboutamazon.com/dims4/default/52e4ef0/2147483647/strip/true/crop/1200x675+0+0/resize/767x431!/quality/90/?url=https%3A%2F%2Famazon-blogs-brightspot.s3.amazonaws.com%2F6f%2F53%2Fdaff0e894356abdbfd01484c7b75%2Faa-shv1-dtf-proteuspov-optimized.gif" alt="Floor Information" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
        </div>
        <!-- Repeat this for other sections as well -->
		    <div id="buildinginfo" class="tool">
        <h2>Building Information</h2>
        <p>Organize and maintain and view building Volumes ETC.</p>
        <img src="https://cdn.dribbble.com/users/5603/screenshots/4234137/boardroom-meeting.gif" alt="Building Information" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
    </div>
    <div id="psolve" class="tool">
        <h2>Problem Solve Tools</h2>
        <p>Enhance interactions with context-aware tools and services.</p>
        <img src="https://i.pinimg.com/originals/b2/9e/0f/b29e0fc7d7859c051fe4b0e2ee4f7078.gif" alt="Problem Solve Tools" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
    </div>
    <div id="optic" class="tool">
        <h2>Optic Manager</h2>
        <p>Same like Vantage but this is a realtime MMA in browser to monitor the Robotic Floor.</p>
        <img src="https://assets.bwbx.io/images/users/iqjWHBFdfxIU/iZW7pKShqhK8/v0/-999x-999.gif" alt="Robotic floor monitoring" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
    </div>
    <div id="apollo" class="tool">
        <h2>Apollo</h2>
        <p>Execute audit for quality, data analysis, and other programmatic needs.</p>
        <img src="https://i.giphy.com/VoksFyW6IYFUI.webp" alt="Apollo Audit" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
    </div>
    <div id="amnesty" class="tool">
        <h2>Amnesty AddBack</h2>
        <p>Add item back in the Bin or Amnesty Shelf.</p>
        <img src="https://sellershipping.com/assets/img/gifs/returns-handling.gif" alt="Amnesty Addback" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);">
    </div>
<div id="amnesty" class="tool">
    <h2>SAT 1 Amnesty Wash 3.5 with Midway</h2>
    <p>Click the button below to download the Amnesty Wash.</p>
    <a href="#" target="_blank">
        <img src="https://cdn.pixabay.com/animation/2022/12/05/10/29/10-29-30-682_512.gif" alt="Amnesty Wash Animation" style="max-width: 100%; border-radius: 10px; box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);" />
        
    </a>
    </div>
    </main>
    <footer>
        <p>&copy; 2025 User Tools made by Christian Sumbillo</p>
    </footer>
</body>
</html>
