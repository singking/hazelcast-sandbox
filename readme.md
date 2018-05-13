


Hazelcast with springboot
https://www.youtube.com/watch?v=82mgDiT_qzM

Common problems with Hazelcast
https://youtu.be/5tpAmWuE3J4?t=11m45s
Listeners: use specific listener and hand off control to another thread ASAP. Caution with the value object exposed in the event listener
http://docs.hazelcast.org/docs/3.8/javadoc/com/hazelcast/core/IMap.html#addEntryListener-com.hazelcast.core.EntryListener-boolean-
Can we not add the listener in the server rather than a client??
http://docs.hazelcast.org/docs/3.5/manual/html/threadingevent.html
https://alexandreesl.com/tag/hazelcast/

http://docs.hazelcast.org/docs/3.7/manual/html-single/index.html#listening-for-multimap-events

http://docs.hazelcast.org/docs/3.7/manual/html-single/index.html#sharding-in-hazelcast

https://www.youtube.com/watch?v=T_vHxDpp9-k

https://stackoverflow.com/questions/11795374/how-do-i-make-hazelcast-to-store-in-my-database-using-mapstore-implementation

http://www.baeldung.com/java-hazelcast

4.3. Create Hazelcast Java Client
Hazelcast client allows us to do all Hazelcast operations without being a member of the cluster. It connects to one of the cluster members and delegates all cluster-wide operations to it.

Let’s create a native client:

ClientConfig config = new ClientConfig();
GroupConfig groupConfig = config.getGroupConfig();
groupConfig.setName("dev");
groupConfig.setPassword("dev-pass");
HazelcastInstance hzClient
  = HazelcastClient.newHazelcastClient(config);
The default username and password to access the cluster are dev and dev-pass. For more details on Hazelcast client, you can check out the following link.



https://github.com/hazelcast/hazelcast/issues/10103

