<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Webhook document</title>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <!-- <link rel="stylesheet" href="style.css"> -->
    <style>
       @import "https://fonts.googleapis.com/css?family=Poppins:300,400,500,600,700";
body {
    font-family: 'Poppins', sans-serif;
    background: #fff;
}

p {
    font-family: 'Poppins', sans-serif;
    /* font-size: 1.1em; */
    font-weight: 300;
    line-height: 1.7em;
    color: #575757;
}

h1,
h2,
h4,
h5,
h6 {
    color: #373737
}

h4 {
    font-size: 16px;
}

a,
a:hover,
a:focus {
    color: inherit;
    text-decoration: none;
    transition: all 0.3s;
}

.navbar {
    padding: 15px 10px;
    background: #fff;
    border: none;
    border-radius: 0;
    margin-bottom: 40px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
}

.navbar-btn {
    box-shadow: none;
    outline: none !important;
    border: none;
}

.line {
    width: 100%;
    height: 1px;
    border-bottom: 1px dashed #ddd;
    margin: 40px 0;
}


/* ---------------------------------------------------
    SIDEBAR STYLE
----------------------------------------------------- */

.wrapper {
    display: flex;
    align-items: stretch;
}

#sidebar {
    min-width: 225px;
    max-width: 250px;
    background: #4a4b50;
    color: #fff;
    transition: all 0.3s;
}

#sidebar.active {
    margin-left: -250px;
}

#sidebar .sidebar-header {
    padding: 20px;
    background: #2b2c2f;
}

.sidebar-header h3 {
    color: #fff
}

#sidebar ul.components {
    padding: 20px 0;
    border-bottom: 1px solid #47748b;
}

#sidebar ul p {
    color: #fff;
    padding: 10px;
}

#sidebar ul li a {
    padding: 10px;
    font-size: 1.1em;
    display: block;
}

#sidebar ul li a:hover {
    color: #fff;
    background: #2b2c2f;
}

#sidebar ul li.active>a,
a[aria-expanded="true"] {
    color: #fff;
    background: #2b2c2f;
}

a[data-toggle="collapse"] {
    position: relative;
}

a[aria-expanded="false"]::before,
a[aria-expanded="true"]::before {
    content: '\e259';
    display: block;
    position: absolute;
    right: 20px;
    font-family: 'Glyphicons Halflings';
    font-size: 0.6em;
}

a[aria-expanded="true"]::before {
    content: '\e260';
}

ul ul a {
    font-size: 0.9em !important;
    padding-left: 30px !important;
    /* background: #6d7fcc; */
}

ul.CTAs {
    padding: 20px;
}

ul.CTAs a {
    text-align: center;
    font-size: 0.9em !important;
    display: block;
    border-radius: 5px;
    margin-bottom: 5px;
}

a.download {
    background: #fff;
    color: #7386D5;
}

a.article,
a.article:hover {
    background: #6d7fcc !important;
    color: #fff !important;
}


/* ---------------------------------------------------
    CONTENT STYLE
----------------------------------------------------- */

#content {
    /* padding: 20px; */
    min-height: 100vh;
    transition: all 0.3s;
}

.bg_grey {
    background: #f1f1f1;
}

.left_sec .bg_grey {
    background: #f1f1f1;
    padding: 15px;
    margin-bottom: 20px;
}

.left_sec {
    background: #fff;
    padding: 20px;
    border-top: 1px dashed #c2cdd3
}

.right_sec {
    background: #e5ebee;
    padding: 40px 30px;
}

.left_sec h1 {
    padding: 15px;
    background: #f1f1f1;
    margin-bottom: 20px;
    font-size: 21px;
    /* border-bottom: 1px solid #ddd; */
}

.right_sec p {
    margin: 10px 0
}

.right_sec h3 {
    padding: 10px 15px;
    background: #c2cdd3;
    margin: 30px 0;
    font-size: 14px;
    padding: 13px;
    border-top: 1px solid #9fa5a8;
    border-bottom: 1px solid #919597;
}

pre {
    background: transparent;
    color: #575757;
    border: none;
    padding: 0
}

table th,
table td {
    font-size: 12px;
}


/* ---------------------------------------------------
    MEDIAQUERIES
----------------------------------------------------- */

.side_bar {
    position: fixed;
    height: 100%;
}

@media (min-width: 768px) {
    .no-padding {
        padding: 0
    }
}

@media (max-width: 768px) {
    #sidebar {
        margin-left: -250px;
    }
    #sidebar.active {
        margin-left: 0;
    }
    #sidebarCollapse span {
        display: none;
    }
}

@media (max-width: 768px) and (max-width:992px) {}
    
    </style>
</head>

<body>
    <div class="wrapper">
        <!-- Sidebar Holder -->
        <div class="col-md-3 col-lg-2 col-sm-3 no-padding">
            <nav id="sidebar" class="side_bar">
                <div class="sidebar-header">
                    <h3>ResponseiQ</h3>
                </div>

                <ul class="list-unstyled components">
                    <!-- <p>Webhooks</p> -->
                    <li class="active">
                        <a href="#pageSubmenu" data-toggle="collapse" aria-expanded="false">Webhooks</a>
                        <ul class="collapse list-unstyled in" id="pageSubmenu">
                            <li><a href="#overview">Overview</a></li>
                            <li><a href="#events">Events</a></li>
                            <li><a href="#callNew">Call New</a></li>
                            <li><a href="#callScheduled">Call Scheduled</a></li>
                            <li><a href="#callMissed">Call Missed</a></li>
                            <li><a href="#callClaimed">Call Claimed</a></li>
                            <li><a href="#callConnected">Call Connected</a></li>
                            <li><a href="#callFinished">Call Finished</a></li>
                        </ul>
                    </li>
                   

                </ul>

               
            </nav>
        </div>

        <!-- Page Content Holder -->
        <div class="col-md-9 col-lg-10 col-sm-9">
            <div id="content">
                <div class="row" id="overview">
                    <div class="col-sm-6  left_sec">
                        <h1>Webhooks</h1>
                        <div class="col-md-12 ">
                            <h4>Overview</h4>
                            <p>When one of these events fired , we'll send you json in your webhook url that you have provided. 
                                All you need is a simple web server that allows to receive incoming POST requests and is able to parse JSON in order to read data.
                            </p>
                        </div>

                        <div class="line col-md-12"></div>
                    </div>
                    <div class="col-sm-6  right_sec">
                        
                     
                        <div class="line col-md-12"></div>

                    </div>
                </div>
                <div class="row" id="events">
                    <div class="col-sm-6  left_sec">
                        <h1>Events</h1>
                      
                        <div class="col-md-12 ">
                        <p>In webhook panel you can select which events you would like to receive.</p>
                            <table class="table table-striped">
                                <thead>
                                    <tr>
                                        <th witdh="20%">Event</th>
                                        <th witdh="80%">Description</th>
                                    </tr>
                                </thead>
                                <tbody>
                                      <tr>
                                        <td>call.new</td>
                                        <td>When new call genrated.</td>
                                    </tr>
                                    <tr>
                                        <td>call.scheduled</td>
                                        <td>When customer scheduled the call.</td>
                                    </tr>
                                    <tr>
                                        <td>call.missed</td>
                                        <td>When there is no available agents.</td>
                                    </tr>
                                    <tr>
                                        <td>call.claimed</td>
                                        <td>When call is claimed by agent.</td>
                                    </tr>
                                    <tr>
                                        <td>call.connected</td>
                                        <td>When call is connected to  the customer.</td>
                                    </tr>
                                    <tr>
                                        <td>call.finished</td>
                                        <td>When call is successfully completed.</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>

                        <div class="line col-md-12"></div>
                    </div>
                    <div class="col-sm-6  right_sec">


                        <div class="line col-md-12"></div>

                    </div>
                </div>
                <div class="row" id ="callNew">
                    <div class="col-sm-6  left_sec">
                        <h1>call.new</h1>
                        <div class="col-md-12 ">
                           
                            <p>This event is fired when customer requested to call.
                            </p>
                        </div>

                        <div class="line col-md-12"></div>
                    </div>
                    <div class="col-sm-6  right_sec">

                        <h3>Response :</h3>
                        <p>
 <pre>
  {
    'event':'call.new'
    'call_id':'142'
    'widget_id':'5000'
    'lead_phone':'+919876543210'
    'visitor_city':'Panchkula'
    'visitor_timezone':'Asia/Kolkata'
    'visitor_url':'https://responseiq.com/'
    'referral_url':''
    'department':''
    'dynamic_number':''
    'gaclientid':'118614583.1553841794'
    'created':'2019-04-15T11:30:01.000Z'
 }                                                  
  </pre>                    
                        </p>

                        <div class="line col-md-12"></div>

                    </div>
                </div>
                <div class="row" id ="callScheduled">
                        <div class="col-sm-6  left_sec">
                            <h1>call.scheduled</h1>
                            <div class="col-md-12 ">
                               
                                <p>This event is fired when a call scheduled by customer.
                                </p>
                            </div>
    
                            <div class="line col-md-12"></div>
                        </div>
                        <div class="col-sm-6  right_sec">
    
                            <h3>Response :</h3>
                            <p>
<pre>      
 {
   "event": "",
   "call_id": "",
   "widget_id": "",
   "lead_phone": "",
   "visitor_city": "",
   "visitor_timezone": "",
   "visitor_url": "",
   "referral_url": "",
   "department": "",
   "dynamic_number": "",
   "scheduled_for": ""
   "created": "",  
 }                                                                                                      
</pre>                                
                            </p>
                     <div class="line col-md-12"></div>
    
                        </div>
                </div>
                <div class="row" id ="callMissed">
                        <div class="col-sm-6  left_sec">
                            <h1>call.missed</h1>
                            <div class="col-md-12 ">
                               
                                <p>This event is fired when a call missed by agents.
                                </p>
                            </div>
    
                            <div class="line col-md-12"></div>
                        </div>
                        <div class="col-sm-6  right_sec">
    
                            <h3>Response</h3>
                            <p>
<pre>      
 {
    'event':'call.missed'
    'call_id':'141'
    'widget_id':'5000'
    'lead_phone':'+919876543210'
    'callstatus':'Missed by customer - agent hangup'
    'retry_attempts':'0'
    'created':'2019-04-12T20:07:46.000Z'
 }   
                                                                                                         
</pre>
                            </p>
    
                            <div class="line col-md-12"></div>
    
                        </div>
                </div>
                <div class="row" id ="callClaimed">
                        <div class="col-sm-6  left_sec">
                            <h1>call.claimed</h1>
                            <div class="col-md-12 ">
                               
                                <p>This event is fired when a call claimed by agent.
                                </p>
                            </div>
    
                            <div class="line col-md-12"></div>
                        </div>
                        <div class="col-sm-6  right_sec">
    
                            <h3>Response :</h3>
                            <p>
<pre>      
 {
    'event':'Widget'
    'call_id':'142'
    'agent_id':'1'
    'widget_id':'5000'
    'lead_phone':'+919876543210'
    'agent_name':'John'
    'agent_email':'john@responseiq.com'
    'agent_phone':'9876543210'
    'agent_extension':''
    'callstatus':'MissedCustomer'
    'created':'2019-04-15T11:30:42.000Z'
 }    
                                                                                                         
 </pre>
                            </p>
    
                            <div class="line col-md-12"></div>
    
                        </div>
                </div>
                <div class="row" id ="callConnected">
                        <div class="col-sm-6  left_sec">
                            <h1>call.connected</h1>
                            <div class="col-md-12 ">
                               
                                <p>This event is fired when a call connected to customer.
                                </p>
                            </div>
    
                            <div class="line col-md-12"></div>
                        </div>
                        <div class="col-sm-6  right_sec">
    
                            <h3>Response :</h3>
                            <p>
<pre>      
 {
   'event':'call.connected'
   'type':'Widget'
   'call_id':'142'
   'agent_id':'1'
   'widget_id':'5000'
   'lead_phone':'+917889096665'
   'callstatus':'Call in progress'
   'retry_attempts':'1'
   'created':'2019-04-15T11:30:54.000Z'
 }   
                                                                                                         
 </pre>
                            </p>
    
                            <div class="line col-md-12"></div>
    
                        </div>
                </div>
                <div class="row" id ="callFinished">
                        <div class="col-sm-6  left_sec">
                            <h1>call.finished</h1>
                            <div class="col-md-12 ">
                               
                                <p>This event is fired when a call was completely finished.
                                </p>
                            </div>
    
                            <div class="line col-md-12"></div>
                        </div>
                        <div class="col-sm-6  right_sec">
    
                            <h3>Response :</h3>
                            <p>
<pre>      
 {
   'event':'call.finished'
   'wtype':'Widget'
   'call_id':'142'
   'agent_id':'1'
   'widget_id':'5000'
   'lead_phone':'+919876543210'
   'recording':'https://storage.googleapis.com/storage.responseiq.com/recordings/50ce2d828ba343f31_lead.wav'
   'duration':'0'
   'retry_attempts':'1'
   'callstatus':'completed'
   'created':'2019-04-15T11:31:22.000Z'
 }         
                                                                                                         
 </pre>
                            </p>
    
                            <div class="line col-md-12"></div>
    
                        </div>
                </div>
            </div>
        </div>
    </div>





    <!-- jQuery CDN -->
    <script src="https://code.jquery.com/jquery-1.12.0.min.js"></script>
    <!-- Bootstrap Js CDN -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

    <script type="text/javascript">
        $(document).ready(function() {
            $('#sidebarCollapse').on('click', function() {
                $('#sidebar').toggleClass('active');
            });
        });
    </script>
</body>

</html>
