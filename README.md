package Server;
import Client.Client;

import java.io.IOException;
import java.net.ServerSocket;
import java.net.Socket;

public class Server {


    public class MultiClientServer {

        public static void main(String[] args) {
            int port = 12345;

            try (ServerSocket serverSocket = new ServerSocket(port)) {
                System.out.println("Server läuft auf Port " + port);

                while (true) {
                    // Neue Client-Verbindung akzeptieren (blockiert bis Verbindung ankommt)
                    Socket clientSocket = serverSocket.accept();
                    System.out.println("Neue Verbindung von " + clientSocket.getRemoteSocketAddress());

                    // Neuen Thread starten, der Client bedient

                }
            } catch (IOException e) {
                System.err.println("Fehler beim Server: " + e.getMessage());
            }
        }
    }
}
