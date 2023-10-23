

<!-- Right sidebar code start -->

        <div  v-if="selectedTools.length > 0"  class="mt-20 fixed right-0 h-[900px] w-[200px] bg-slate-600 p-5 m-4">

          <h1 class="text-white "> Selected Tool:</h1>

          <div v-for="(tools, index) in selectedTools" :key="index" >

            <div class="tools m-5">

              {{ tools }}

            </div>  

            <hr>

           

          </div>

          <button type="button" @click.prevent="toggleModal" class="mt-5 text-sm text-blue-100 bg-gray-800 p-3  rounded-full focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600" >

            install                      

        </button>

         </div>

         <!-- Rightsidebar code end -->

[Yesterday 8:51 AM] Ashish Sahu

append this code to you templete

[Yesterday 8:52 AM] Ashish Sahu

Here you can find where You have to append this code

 

  <div class="flex p-4 sm:ml-64">

        <div class=" border-gray-200  rounded-lg dark:border-gray-700 ">   

            <div class="rounded bg-gray-50 dark:bg-gray-800">         

            <section class="shadow-inner" id="HOM">

                <h1 class="txt1">Welcome to our DURGA Platform</h1>

                <div class="txt2">Guarding with Open Source: Your Digital Safehouse</div>

            </section> <hr>

        

            <section class="shadow-inner" id="LI">

                <h1 class=""> Log Ingestion</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    <div class="border-2 border-gray-200 border-dashed">

                        <div class="tool" :style="{'background-color': selectedTools.includes('fluentd') ? 'pink' : 'initial'}" >

                          <label for="Fluentd">

                            <input v-model="selectedTools" class="hidden" type="checkbox" name="Fluentd" id="Fluentd" value="fluentd"> Fluentd  

                                <p class="tool-info">Fluentd simplifies data collection, enabling efficient log aggregation and flexible data routing. It plays a crucial role in log management, helping organizations centralize and analyze logs effectively. <a href="https://docs.fluentd.org/"><span class="text-gray-600 ">Read more </span></a></p>

                                <img class="tool_img" src=" static/fluentdd.png " alt="Fluentd Logo">

                             </label>

                            </div>

                        </div>

                    <div class="border-2 border-gray-200 border-dashed"  :style="{'background-color': selectedTools.includes('filebeat') ? 'pink' : 'initial'}">

                        <div class="">

                          <label for="Filebeat">

                                    <input v-model="selectedTools" type="checkbox" class="hidden" name="Filebeat" id="Filebeat" value="filebeat"> Filebeat

                                    <p class="tool-info">A lightweight member of the Elastic Stack, Filebeat efficiently ships logs to Elasticsearch. It ensures real-time log analysis and monitoring, enhancing observability and operational insights. <a href="https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-overview.html">Read more</a></p>

                                    <img class="tool_img" src=" static/filebeat.png" alt="Filebeat Logo">

                        </label></div>

                    </div>

                    <div class="border-2 border-gray-200 border-dashed">

                        <div class=""><label for="Rsyslog">

                                        <input v-model="selectedTools" type="checkbox" name="Rsyslog" id="Rsyslog" value="rsyslog"> Rsyslog

                                        <p class="tool-info">Rsyslog is a reliable open-source logging system. It centralizes log management, simplifying monitoring and troubleshooting of system and application events for organizations. <a href="https://www.rsyslog.com/doc/master/index.html">Read more</a></p>                 

                                        <img class="tool_img" src=" static/rsyslog.png " alt="Rsyslog Logo">

                        </label></div>

                    </div>  

                </div>

            </section> <hr>

        

            <section class="shadow-inner" id="LA">

                <h1 class="">Log Analysis</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                     <div class="tool border-2 border-gray-200 border-dashed"><label for="Graylog">

                        <input v-model="selectedTools"  type="checkbox" name="Graylog" id="Graylog"  value="graylog" > Graylog

                        <p class="tool-info">Graylog, with its user-friendly interface, offers comprehensive log management and analysis. It optimizes log storage, search, and alerting, making it a valuable tool for both security and operations. <a href="https://go2docs.graylog.org/5-1/home.htm">Read more</a></p>

                        <img class="tool_img" src=" static/graylog.png" alt="">

                      </label></div>

                     

                      <div class="border-2 border-gray-200 border-dashed"><label for="Splunk">

                        <input v-model="selectedTools" type="checkbox" name="Splunk" id="Splunk" value="splunk"> Splunk HEC

                        <p class="tool-info">Splunk HEC facilitates HTTP-based log and event data ingestion. It enhances real-time data analysis, offering critical insights for organizations using Splunk for log management and monitoring. <a href="https://docs.splunk.com/Documentation/Splunk/9.1.1/Data/UsetheHTTPEventCollector">Read more</a></p>

                        <img class="tool_img" src=" static/splunk.png" alt="">

                      </label></div>

                   

                      <div class="border-2 border-gray-200 border-dashed"><label for="LogAnalyzer">

                        <input v-model="selectedTools" type="checkbox" name="LogAnalyzer" id="LogAnalyzer" value="logAnalyzer"> LogAnalyzer (formerly known as phpLogCon)

                        <p class="tool-info">LogAnalyzer is a web-based log management tool designed for effective log analysis. It simplifies system issue monitoring and troubleshooting, ensuring robust log management. <a href="https://loganalyzer.adiscon.com/doc/">Read more</a></p>

                        <img class="tool_img" src=" static/loganalyzer.png" alt="">

                      </label></div>

                </div>    

            </section><hr>

            <section class="shadow-inner" id="BS">

                <h1  class="">Backend Storage </h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                    <div class="tool"><label for="WazuhIndexer">

                    <input v-model="selectedTools" type="checkbox" name="WazuhIndexer" id="WazuhIndexer" value="wazuhIndexer"> Wazuh Indexer

                    <p class="tool-info">A vital part of the Wazuh platform, the Wazuh Indexer handles indexing and querying of security data. It forms the cornerstone for effective threat detection and response strategies. <a href="https://documentation.wazuh.com/current/installation-guide/wazuh-indexer/index.html">Read more</a></p>

                    <img src=" static/wazuhindexer.png" alt="Wazuh Logo">

                    </label></div>

                

                    <div class="tool"><label for="Elasticsearch">

                    <input v-model="selectedTools" type="checkbox" name="Elasticsearch" id="Elasticsearch" value="elasticsearch"> Elasticsearch

                    <p class="tool-info">ElasticSearch, a distributed search and analytics engine, excels in storing and searching large data volumes. Its commonly utilized in ELK (Elasticsearch, Logstash, Kibana) stacks for diverse use cases <a href="https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html">Read more</a></p>

                    <img src=" static/elasticsearch.png " alt="Wazuh Logo">

                    </label></div>

                    

                    <div class="tool"><label for="Apache">

                    <input v-model="selectedTools" type="checkbox" name="Apache" id="Apache" value="apache_cassandra"> Apache Cassandra

                    <p class="tool-info">Apache Cassandra is a highly scalable NoSQL database, ideal for managing extensive data volumes. Its focus on high availability and fault tolerance makes it an excellent choice for organizations. <a href="https://cassandra.apache.org/doc/latest/">Read more</a></p>

                    <img src="static/apache.png" alt="Wazuh Logo">

                    </label></div>

                </div>

            </section><hr>

            <section id="V">

                <h1  class="">Visualization</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section class="shadow-inner" id="IE">

                <h1  class="">Intelligent Enrichment</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section class="shadow-inner" id="TDP">

                <h1  class="">Tread Detection And Prevention</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section class="shadow-inner" id="CM">

                <h1 class="">Case Management</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section class="shadow-inner" id="ATO">

                <h1 class="">Log Automate</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section class="shadow-inner" id="INV">

                <h1 class="">Investigation</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

            <section  class="shadow-inner" id="HM">

                <h1 class="">Health Monitoring</h1>

                <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

                    

                </div>

            </section><hr>

        </div>

        </div>

        <!-- Right sidebar code start -->

        <div  v-if="selectedTools.length > 0"  class="mt-20 fixed right-0 h-[900px] w-[200px] bg-slate-600 p-5 m-4">

          <h1 class="text-white "> Selected Tool:</h1>

          <div v-for="(tools, index) in selectedTools" :key="index" >

            <div class="tools m-5">

              {{ tools }}

            </div>  

            <hr>

           

          </div>

          <button type="button" @click.prevent="toggleModal" class="mt-5 text-sm text-blue-100 bg-gray-800 p-3  rounded-full focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600" >

            install                      

        </button>

         </div>

         <!-- Rightsidebar code end -->

    </div>



Modify the section style also

 

 

section {

   width: 80%;

    opacity: 0;

    transform: translateY(5px);

    transition: opacity 0.6s ease, transform 0.6s ease;

}
