## Lab Report 2
Yutong Guo<br>
A16269813<br>
### CODE
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;
import java.util.List;

class Handler implements URLHandler {
    private final List<String> messages = new ArrayList<>();

    @Override
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "Hello, here are the list of items stored: " + String.join("\n", messages);
        } else if (url.getPath().contains("/add-message")) {
            String query = url.getQuery();
            if (query != null && query.startsWith("s=")) {
                String newMessage = query.substring(2);
                messages.add((messages.size() + 1) + ". " + newMessage);
                return String.join("\n", messages);
            } else {
                return "Invalid request!";
            }
        } else {
            return "404 Not Found!";
        }
    }
}

public class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
