# Http-Background-Worker-Android

Copy Both files in your Android Project Main Folder.
and use following code to connect to Remote Server in Background to fetch and post data. :)


String link = "www.google.com"; //your Link
Context c; // Your Activity Context
String data[] = new String[]{"VAR1_NAME","VAR1_VALUE","VAR2_NAME","VAR2_VALUE"}; // POST any amount of var and there values. size should be even


MyHttpClient myHttpClient = new MyHttpClient(c, link,data);
                                        myHttpClient.execute();
                                        myHttpClient.callback = new MyCallback() {
                                            @Override
                                            public void callbackCall() {
                                                String result = myHttpClient.result; //Result from your link
                                            }
                                        };
