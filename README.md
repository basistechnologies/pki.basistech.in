# Cryptographic Operations Tester API Reference Guide V 2.0

Java Script API Reference Document

## 1. Sign Data
+ Mode:	Detached
+ Input Type:		Data
+ API:	
  ```javascript
  Sign (data, true);
  ```
+ Example:
  ```javascript
  Sign(document.getElementById('sign-text').value,document.getElementById("r1").checked);
  Sign('example data to sign', true);
  ```
+ Output:		
  ```json
  {"data":"Du1SAjmN2ILGZl0p+lOjeg2/MaAOM+4ced6nV5bU0aLdZAsKLpkMZgc6CpP8ShzLo9ymxlLnsa2NbM0pHZua75B7OnxBFzGNCU5RYLwKeEdr41KVERHmJgRlcUs1Yu4yfb3ot1rfeUZBZaDTCAcJgi4cfzcUrgAGLE3RTk  ZONyvqrXwPESRrTF/aKTbZxT7XTq4p0D7SofxEN5nTJoAheguXIxGw5oomHJp4mfL6rBMIfwmq9EFMlXxC/mslrv0Hh6DUWKnPYJdO1XTeo3PgyVkU2yWIuwA7jzG/0V7DehOPHs8Ym0Cu6TaGW8L4ffJJQyRwvcU1K2BvZF/xJl9LMA==","OP":"sign"}
  ```
  
## 2. Sign Data
+ Mode:		Enveloped
+ Input Type:		Data
+ API:	
  ```javascript
  Sign (data, false);
  ```
+ Example:
  ```javascript
  Sign(document.getElementById('sign-text').value,document.getElementById("r1").checked);
  Sign('example data to sign', false);
  ```
+ Output:		
  ```json
  {"data":"MIIFsAYJKoZIhvcNAQcCoIIFoTCCBZ0CAQExCzAJBgUrDgMCGgUAMCMGCSqGSIb3DQEHAaAWBBRleGFtcGxlIGRhdGEgdG8gc2lnbqCCA7EwggOtMIIClaADAgECAgQpfGHPMA0GCSqGSIb3DQEBCwUAMH8xCzAJBgNVBAYTAk5MMQswCQYDVQQIEwJHQTEpMCcGA1UEBxMgMjI1IEMgQS5KLkMgQm9zZSBSb2FkIEtPTEtBVEEtMjAxEjAQBgNVBAoTCU1TVEMgTHRkLjESMBAGA1UECxMJTVNUQyBMdGQuMRAwDgYDVQQDEwdNU1RDRFMxMB4XDTE0MDgyODA0NDgzMVoXDTI0MDkwOTA0NDgzMVowfzELMAkGA1UEBhMCTkwxCzAJBgNVBAgTAkdBMSkwJwYDVQQHEyAyMjUgQyBBLkouQyBCb3NlIFJvYWQgS09MS0FUQS0yMDESMBAGA1UEChMJTVNUQyBMdGQuMRIwEAYDVQQLEwlNU1RDIEx0ZC4xEDAOBgNVBAMTB01TVENEUzEwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCZawi0OewRjdqQ8KFfKR8B/doCw37uy/gHksR6ACLtwmlnRNWaA8PELeo9mxWqQRsOjp99vlRR+9GUvQptMZvYlZw3XmCIhUkZt4IfQPem6jXeXoZHNReUvJ4yjQtNwJotQFNJuv/IkCb0UjHyj/6Z1lsjy0gQ7l/iGR56CDcsnVdmsSnHgn6Q/AoLlJF7RHfLG05P/sHGHCLtfZcgSWXaU5SRxzrczSbCtfDAcacDhbxaMWbtGVqTaV1FuLNfI7kvu46SG+CbTyv9CrBrRzQX+JQXl7xlkuEUlRkazarYmjNoorPy7jN7hTq4PVRw+KhaDSkmGYB2RVPwJeEAPoOvAgMBAAGjMTAvMA4GA1UdDwEB/wQEAwIGwDAdBgNVHQ4EFgQUAZmqmwkemTZ3qgvckz6CI5dO/YkwDQYJKoZIhvcNAQELBQADggEBAHDX2+9EmT6Hw5uG75tYQepBXzkaqPQ2SFhcl2qvzV3Kf+J8vQ/go3UEQB28hbVNegLXKQ6q0FAbHiUOevZb/T5wfhP7RLJacXNGZZNg/Gq5nlq+mOE/XfkoWAzATEWQYXjnlpJopPYQODkoAb3ExQMvP6vVnyMaNrI+GYp06ghoBv5m5xqpz0MBAIkbHu4jNAJ9qXcAoiVKhwpAHTQ2hjx5oWQNvHv5PYpUa3WH1lAKQ0B9awYJliJmgca/m3l4/QHlOmkq/uqlIY1dIRoLcIXMfCv3LA0rSM7tWqWm0tsvOJuIFeTsC6HtD8aaDSMdKdRoJ4u2aqtwULsmntAL2UcxggGvMIIBqwIBATCBhzB/MQswCQYDVQQGEwJOTDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBLT0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRkLjEQMA4GA1UEAxMHTVNUQ0RTMQIEKXxhzzAJBgUrDgMCGgUAMA0GCSqGSIb3DQEBAQUABIIBAA7tUgI5jdiCxmZdKfpTo3oNvzGgDjPuHHnep1eW1NGi3WQLCi6ZDGYHOgqT/Eocy6PcpsZS57GtjWzNKR2bmu+Qezp8QRcxjQlOUWC8CnhHa+NSlRER5iYEZXFLNWLuMn296Lda33lGQWWg0wgHCYIuHH83FK4ABixN0U5GTjcr6q18DxEka0xf2ik22cU+106uKdA+0qH8RDeZ0yaAIXoLlyMRsOaKJhyaeJny+qwTCH8JqvRBTJV8Qv5rJa79B4eg1Fipz2CXTtV03qNz4MlZFNsliLsAO48xv9Few3oTjx7PGJtAruk2hlvC+H3ySUMkcL3FNStgb2Rf8SZfSzA=","OP":"signA"}
  ```

## 3.		Verify Data
+ Mode:		Detached
+ Input Type:		Data
+ API: 
  ```javascript
  Verify (signedData, true);
  ```
+ Example:		
  ```javascript
  Verify(document.getElementById('sign-text').value,document.getElementById('signed-text').value,document.getElementById("r1").checked);
  Verify('Du1SAjmN2ILGZl0p+lOjeg2/MaAOM+4ced6nV5bU0aLdZAsKLpkMZgc6CpP8ShzLo9ymxlLnsa2NbM0pHZua75B7OnxBFzGNCU5RYLwKeEdr41KVERHmJgRlcUs1Yu4yfb3ot1rfeUZBZaDTCAcJgi4cfzcUrgAGLE3RTkZONyvqrXwPESRrTF/aKTbZxT7XTq4p0D7SofxEN5nTJoAheguXIxGw5oomHJp4mfL6rBMIfwmq9EFMlXxC/mslrv0Hh6DUWKnPYJdO1XTeo3PgyVkU2yWIuwA7jzG/0V7DehOPHs8Ym0Cu6TaGW8L4ffJJQyRwvcU1K2BvZF/xJl9LMA==',true)
  ```
+Output:		
  ```json
  {"data":"True","OP":"verify"}
  ```

## 4. Verify Data
+ Mode:		Enveloped
+ Input Type:		Data
+ API:		
  ```javascript
  Verify(signedData, false);
  ```
+ Example:	
  ```javascript
  Verify(document.getElementById('sign-text').value,document.getElementById('signed-text').value,document.getElementById("r1").checked);
  Verify('MIIFsAYJKoZIhvcNAQcCoIIFoTCCBZ0CAQExCzAJBgUrDgMCGgUAMCMGCSqGSIb3DQEHAaAWBBRleGFtcGxlIGRhdGEgdG8gc2lnbqCCA7EwggOtMIIClaADAgECAgQpfGHPMA0GCSqGSIb3DQEBCwUAMH8xCzAJBgNVBAYTAk5MMQswCQYDVQQIEwJHQTEpMCcGA1UEBxMgMjI1IEMgQS5KLkMgQm9zZSBSb2FkIEtPTEtBVEEtMjAxEjAQBgNVBAoTCU1TVEMgTHRkLjESMBAGA1UECxMJTVNUQyBMdGQuMRAwDgYDVQQDEwdNU1RDRFMxMB4XDTE0MDgyODA0NDgzMVoXDTI0MDkwOTA0NDgzMVowfzELMAkGA1UEBhMCTkwxCzAJBgNVBAgTAkdBMSkwJwYDVQQHEyAyMjUgQyBBLkouQyBCb3NlIFJvYWQgS09MS0FUQS0yMDESMBAGA1UEChMJTVNUQyBMdGQuMRIwEAYDVQQLEwlNU1RDIEx0ZC4xEDAOBgNVBAMTB01TVENEUzEwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCZawi0OewRjdqQ8KFfKR8B/doCw37uy/gHksR6ACLtwmlnRNWaA8PELeo9mxWqQRsOjp99vlRR+9GUvQptMZvYlZw3XmCIhUkZt4IfQPem6jXeXoZHNReUvJ4yjQtNwJotQFNJuv/IkCb0UjHyj/6Z1lsjy0gQ7l/iGR56CDcsnVdmsSnHgn6Q/AoLlJF7RHfLG05P/sHGHCLtfZcgSWXaU5SRxzrczSbCtfDAcacDhbxaMWbtGVqTaV1FuLNfI7kvu46SG+CbTyv9CrBrRzQX+JQXl7xlkuEUlRkazarYmjNoorPy7jN7hTq4PVRw+KhaDSkmGYB2RVPwJeEAPoOvAgMBAAGjMTAvMA4GA1UdDwEB/wQEAwIGwDAdBgNVHQ4EFgQUAZmqmwkemTZ3qgvckz6CI5dO/YkwDQYJKoZIhvcNAQELBQADggEBAHDX2+9EmT6Hw5uG75tYQepBXzkaqPQ2SFhcl2qvzV3Kf+J8vQ/go3UEQB28hbVNegLXKQ6q0FAbHiUOevZb/T5wfhP7RLJacXNGZZNg/Gq5nlq+mOE/XfkoWAzATEWQYXjnlpJopPYQODkoAb3ExQMvP6vVnyMaNrI+GYp06ghoBv5m5xqpz0MBAIkbHu4jNAJ9qXcAoiVKhwpAHTQ2hjx5oWQNvHv5PYpUa3WH1lAKQ0B9awYJliJmgca/m3l4/QHlOmkq/uqlIY1dIRoLcIXMfCv3LA0rSM7tWqWm0tsvOJuIFeTsC6HtD8aaDSMdKdRoJ4u2aqtwULsmntAL2UcxggGvMIIBqwIBATCBhzB/MQswCQYDVQQGEwJOTDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBLT0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRkLjEQMA4GA1UEAxMHTVNUQ0RTMQIEKXxhzzAJBgUrDgMCGgUAMA0GCSqGSIb3DQEBAQUABIIBAA7tUgI5jdiCxmZdKfpTo3oNvzGgDjPuHHnep1eW1NGi3WQLCi6ZDGYHOgqT/Eocy6PcpsZS57GtjWzNKR2bmu+Qezp8QRcxjQlOUWC8CnhHa+NSlRER5iYEZXFLNWLuMn296Lda33lGQWWg0wgHCYIuHH83FK4ABixN0U5GTjcr6q18DxEka0xf2ik22cU+106uKdA+0qH8RDeZ0yaAIXoLlyMRsOaKJhyaeJny+qwTCH8JqvRBTJV8Qv5rJa79B4eg1Fipz2CXTtV03qNz4MlZFNsliLsAO48xv9Few3oTjx7PGJtAruk2hlvC+H3ySUMkcL3FNStgb2Rf8SZfSzA=', false)
  ```
+ Output:		
  ```json
  {"data":"Signature : verified The eclosed plain text:example data to sign","OP":"verifyA"}
  ```

## 5. Encrypt Data
+ Mode:		Detached
+ Input Type:		Data
+ API: 
  ```javascript
  Encrypt (data, true);
  ```
+ Example:		
  ```javascript
  Encrypt(document.getElementById('sign-text').value,document.getElementById("r1").checked);
  Encrypt('example data to encrypt', true);
  ```
+ Output:		
  ```json
  {"data":"eneTuJn1zgAtEmOujwDWp887AO917aK1OzWrnnapVlALDDlwtjbU6RNA2nXQlSvK5F8xW2i0Nikc7PCBxFw8ZIv7VnDPuZS1AEkYtyQtT8ZRI6SG945mPDn17HcGccs4EziIChsatNg7T6PqNSEi6sFGHIe/+4iFirP1XXPPZqVVGUqEE6kMX35xnQlh323nOgdLREvU69wdogzokoYmAVtiHPlYIvxoN8a8Phskq5zU+HzD710HqGerJuct7DjiwHUsWajqSqGag3O60BLMorZj9g7DnU/2rEfQfWxcT42Mp+kJ08ZbMPpqvjy8wZlP6Zb7Zn8dxfz98FJAWZGLWw==","OP":"encrypt"}
  ```
  
## 6. Encrypt Data
+ Mode:		Enveloped
+ Input Type:		Data
+ API:	
  ```javascript
  Encrypt (data, false);
  ```
+ Example:		
  ```javascript
  - Encrypt(document.getElementById('sign-text').value,document.getElementById("r1").checked);
  - Encrypt('example data to encrypt', false);
  ```
+ Output:		
  ```json
  {"data":"MIIB+wYJKoZIhvcNAQcDoIIB7DCCAegCAQAxggGkMIIBoAIBADCBhzB/MQswCQYDVQQGEwJOTDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBLT0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRkLjEQMA4GA1UEAxMHTVNUQ0RTMQIEKXxhzzANBgkqhkiG9w0BAQEFAASCAQCQOnWDIYaXTSrZIZQTk8k4Gm+ofDVgFtWH2XAqYhKE0NXahJBPev2FmiYh3uMfFK1FZtrn6+AXh1SerhUQVoJpew+mgds51qP/oyKuFVYmc+W4rnt7Gm3NM+h7TShURV0WRNbty+SPL4PrzcoL/PgucTRUBM2uBGUThj/IjR7gSUdCSs0RFPoM010wctQq8ojhGzHVM3OKV0E8u7YJbG+y3ctW05FMHfkHuKiX858BXQRUxENJ39QsuM38nA5GDIB86O6Q6Tg83Hq+GeOTLcBpWGi5FwA1xVXqz3CdJvHlBkHRog4WT/COIGl0W0D3AGvIjrTfyyXL29e2rdUg4oX7MDsGCSqGSIb3DQEHATAUBggqhkiG9w0DBwQITfaz+b1/JE2AGJ6LP7yyOJWlZmnQzB3PCH4yxbGJ+BdCdQ==","OP":"encryptA"}
    ````

## 7. Decrypt Data
+ Mode:		Detached
+ Input Type:		Data
+ API: 
  ```javascript
  Decrypt (data, false);
  ```
+ Example:
  ```javascript
  Decrypt(document.getElementById('signed-text').value,document.getElementById("r1").checked);
  Decrypt('eneTuJn1zgAtEmOujwDWp887AO917aK1OzWrnnapVlALDDlwtjbU6RNA2nXQlSvK5F8xW2i0Nikc7PCBxFw8ZIv7VnDPuZS1AEkYtyQtT8ZRI6SG945mPDn17HcGccs4EziIChsatNg7T6PqNSEi6sFGHIe/+4iFirP1XXPPZqVVGUqEE6kMX35xnQlh323nOgdLREvU69wdogzokoYmAVtiHPlYIvxoN8a8Phskq5zU+HzD710HqGerJuct7DjiwHUsWajqSqGag3O60BLMorZj9g7DnU/2rEfQfWxcT42Mp+kJ08ZbMPpqvjy8wZlP6Zb7Zn8dxfz98FJAWZGLWw==', true)
  ```
+ Output:		
  ```json
  {"data":"example data to encrypt","OP":"decrypt"}
  ```
## 8. Decrypt Data
+ Mode:		Enveloped
+ Input Type:		Data
+ API:		
  ```javascript
  Decrypt (data, true);
  ```
+ Example:
  ```javascript
  Decrypt(document.getElementById('signed-text').value,document.getElementById("r1").checked);
  Decrypt('MIIB+wYJKoZIhvcNAQcDoIIB7DCCAegCAQAxggGkMIIBoAIBADCBhzB/MQswCQYDVQQGEwJOTDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBLT0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRkLjEQMA4GA1UEAxMHTVNUQ0RTMQIEKXxhzzANBgkqhkiG9w0BAQEFAASCAQCQOnWDIYaXTSrZIZQTk8k4Gm+ofDVgFtWH2XAqYhKE0NXahJBPev2FmiYh3uMfFK1FZtrn6+AXh1SerhUQVoJpew+mgds51qP/oyKuFVYmc+W4rnt7Gm3NM+h7TShURV0WRNbty+SPL4PrzcoL/PgucTRUBM2uBGUThj/IjR7gSUdCSs0RFPoM010wctQq8ojhGzHVM3OKV0E8u7YJbG+y3ctW05FMHfkHuKiX858BXQRUxENJ39QsuM38nA5GDIB86O6Q6Tg83Hq+GeOTLcBpWGi5FwA1xVXqz3CdJvHlBkHRog4WT/COIGl0W0D3AGvIjrTfyyXL29e2rdUg4oX7MDsGCSqGSIb3DQEHATAUBggqhkiG9w0DBwQITfaz+b1/JE2AGJ6LP7yyOJWlZmnQzB3PCH4yxbGJ+BdCdQ==', false)
  ```
+ Output:		
  ```json
  {"data":"example data to encrypt","OP":"decryptA"}
  ```

## 9. Encrypt using Symmetric Key 
+ Mode:		
+ Input Type:		Data
+ API: 
  ```javascript
  EncryptUsingKey (plainText, symKey, IV);
  ```
+ Example:		
  ```javascript
  - EncryptUsingKey(document.getElementById('signed-text').value,document.getElementById('sign-text').value, document.getElementById('result-text').value);
  - EncryptUsingKey('example data to encrypt','25lIT2BMrR6QBongcy+hblxQ7yncoN8FcgVEJ0C+AwU=','X+8a/v9zkNSPi3RQt0mjVw==')
  ```
+ Output:		
  ```json
  {"data":"{\"Key\":\"25lIT2BMrR6QBongcy+hblxQ7yncoN8FcgVEJ0C+AwU=\",\"IV\":\"X+8a/v9zkNSPi3RQt0mjVw==\",\"PlainText\":\"example data to encrypt\",\"CypherText\":\"g3gNMzcGIZUYQEo6MVPJYrss6e6T74ggiDy6/QLidGo=\"}","OP":"encryptT"}
  ```

## 10. Decrypt using Symmetric Key 
+ Mode:		
+ Input Type:		Data
+ API:	
  ```javascript
  EncryptUsingKey (cypherText, symKey, IV);
  ```
+ Example:		
  ```javascript
  DecryptUsingKey(document.getElementById('signed-text').value,document.getElementById('sign-text').value, document.getElementById('result-text').value);
  DecryptUsingKey('g3gNMzcGIZUYQEo6MVPJYrss6e6T74ggiDy6/QLidGo=', '25lIT2BMrR6QBongcy+hblxQ7yncoN8FcgVEJ0C+AwU=', 'X+8a/v9zkNSPi3RQt0mjVw==')
+ Output:		
  ```json
  {"data":"{\"Key\":\"25lIT2BMrR6QBongcy+hblxQ7yncoN8FcgVEJ0C+AwU=\",\"IV\":\"X+8a/v9zkNSPi3RQt0mjVw==\",\"PlainText\":\"example data to encrypt\",\"CypherText\":\"g3gNMzcGIZUYQEo6MVPJYrss6e6T74ggiDy6/QLidGo=\"}","OP":"encryptP"}
  ```

## 11. Encrypt Using Public Key certificate passed as parameter 
+ Mode:		Enveloped
+ Input Type:		Data
+ API:		
  ```javascript
  EncryptUsingPublicKeyCertficate (publicKeyCertificate, plaintext);
  ```
+ Example:	
  ```javascript
  - EncryptUsingPublicKeyCertficate(document.getElementById('signed-text').value,document.getElementById('sign-text').value);

  - EncryptUsingPublicKeyCertficate('example text to encrypt', ' -----BEGIN CERTIFICATE-----  MIIDrTCCApWgAwIBAgIEPqtYczANBgkqhkiG9w0BAQsFADB/MQswCQYDVQQGEwJO  TDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBL  T0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRk  LjEQMA4GA1UEAxMHTVNUQ0RTMTAeFw0xNDA5MDQxMjMzMThaFw0yNDA5MTYxMjMz  MThaMH8xCzAJBgNVBAYTAk5MMQswCQYDVQQIEwJHQTEpMCcGA1UEBxMgMjI1IEMg  QS5KLkMgQm9zZSBSb2FkIEtPTEtBVEEtMjAxEjAQBgNVBAoTCU1TVEMgTHRkLjES  MBAGA1UECxMJTVNUQyBMdGQuMRAwDgYDVQQDEwdNU1RDRFMxMIIBIjANBgkqhkiG  9w0BAQEFAAOCAQ8AMIIBCgKCAQEAlhHhKByO9QqNiyW0l0QLAoutnkTY/iyFM6np  hEzOoYD0ndsQ3nHmkkxgO7CypxUuO81vJUkeYJ04KZUXEpaqwpTWIuurY6a8jneO  BNyuXcmZJAQSf+jS0oS5gGZ5anvTsGt0Trut8zzNaWzhNHqZ0jcH5zVe5R2SyKxL  iabwmcbT+KI9jXmn2NgnaMxz6T+bw8ePhMQwHSe8dDThcQlzlwv7guy35o/vg/T6  yZ2QL2YNOhCA4GNp8IYbE872vcFY5Q87pcSunbUtp9Fg+rkzTtVmywY7E7ovQJi6  o6F+qpYdzmT+3lDTeXL0wwE2LSsT9R6D7fn6HhVR5hN1HSYMywIDAQABozEwLzAO  BgNVHQ8BAf8EBAMCBSAwHQYDVR0OBBYEFGxljjqrpRS45Zr+ltqPdqHC9MgFMA0G  CSqGSIb3DQEBCwUAA4IBAQBponZzKBwP9mcPwshigZi2LO9biAM1SlrquuFgkeTE  6tscZAsdNrR+1B3AcFFXwNV6kmH7j8o+ZZuKpLo9leHDuRjdCbGrOpKsoqzppjkb  B9lkRg0steiEt6ENsDu+U92Gs/OUTPRzLUAdBqtsaHnrGqgS+zrVwJYgQHO6vHzL  QtHtAu+67Ax8Q/lEATTOFXHku448jf1T3siomVYJkJtPN2edR1xgWD4t04l0lg/Z  /ebeLyEfzYYymmxtZRoHw4hFbN6DN51Qj7/bhQxPHbQfKp3A1/wWAMv35yzMczFd  gCjOZ/Qyw609arAifJs1+maiKfOJnUxHKojHH+bz83+d  -----END CERTIFICATE-----  ');
  ```
+ Output:	
  ```json
  {"data":"MIIB+wYJKoZIhvcNAQcDoIIB7DCCAegCAQAxggGkMIIBoAIBADCBhzB/MQswCQYDVQQGEwJOTDELMAkGA1UECBMCR0ExKTAnBgNVBAcTIDIyNSBDIEEuSi5DIEJvc2UgUm9hZCBLT0xLQVRBLTIwMRIwEAYDVQQKEwlNU1RDIEx0ZC4xEjAQBgNVBAsTCU1TVEMgTHRkLjEQMA4GA1UEAxMHTVNUQ0RTMQIEPqtYczANBgkqhkiG9w0BAQEFAASCAQAKBCcPh0Hk9g+8vIVyxl+DKGFAWRRq4RVi7+/5gIlyjEEB1T8C2D/4UHR6UHNEJa+KxtA9Y02D508416axcJsLqeUCaW9Y8FfPZDX8hpUZZLVHpTCQNGTOkh5elOH7HLNjdIOp5CakzdLD8hq67zW6veNs8N+8i3PAHyRWkDt9xa5cYWcUZnoKnvTbHvJsA/Ivn6l+q6fgKKCkDpQIg0xAIyIiCc0UYqD2d/FYMZD+RV2Y2F0kNu6/pUu0XzYjYeFtxEQsBgnVo4ABvRVIUApUS1G882yryOY/s+AJG1zc3DM5umiMG8CXhnLMTn1Zf1wApfVARJGE4zuN/Zy3EZcdMDsGCSqGSIb3DQEHATAUBggqhkiG9w0DBwQIFc3PHOgf3FaAGMBg96AxpVnLXFyAVdjH/UqtPWw1GUavCg==","OP":"encryptP"}
  ```
## 12. Sign File
+ Mode:		
+ Input Type:		File
+ API:	
  ```javascript
  FileSign();
  ```
+ Call:		
  ```javascript
  FileSign();
  ```
+ Output:		
  ```json
  {"data":"WrZVhBqwqQ/GPkuwtwZWn8FeZw9w65J6WdNzVMsX6Ea+cQ8pTkzPQOhDInaUCEN/J6N6+ApdMKNeT79Azh1rgT+bTQdE1sDd/5TBOU0Lv9eyhkVHX44C7fRkjk2PReJbIa66WfZg7KBbXG7cByArB0CYfUvP4639t0bA7V2UVXixLdaQZSsngcuOwjRF2K8zGd4vVURWybTtt8i8eBwXHqezp2OiaWdRKmsD/8LVrc6V3rkW/66YJ9kG/aNze06X1LrcSregCw302SzcCfpqGP6jBJqWIm6XoAujeHOjZ7MHjE0XX5yEKnM2uq4Be/ShxsXikuy3kOTkaG79X44o7w==","OP":"FileSign"}
  ```
## 13. Verify Signed File
+ Mode:		
+ Input Type:		File
+ API:		
  ```javascript
  FileVerify(fileSignature);
  ```
+ Example:		
  ```javascript
  FileVerify(document.getElementById('file-output').value);
  FileVerify ( 'WrZVhBqwqQ/GPkuwtwZWn8FeZw9w65J6WdNzVMsX6Ea+cQ8pTkzPQOhDInaUCEN/J6N6+ApdMKNeT79Azh1rgT+bTQdE1sDd/5TBOU0Lv9eyhkVHX44C7fRkjk2PReJbIa66WfZg7KBbXG7cByArB0CYfUvP4639t0bA7V2UVXixLdaQZSsngcuOwjRF2K8zGd4vVURWybTtt8i8eBwXHqezp2OiaWdRKmsD/8LVrc6V3rkW/66YJ9kG/aNze06X1LrcSregCw302SzcCfpqGP6jBJqWIm6XoAujeHOjZ7MHjE0XX5yEKnM2uq4Be/ShxsXikuy3kOTkaG79X44o7w==' )
  ```
+ Output:		
  ```json
  {"data":"True","OP":"FileVerify"}
  ```

## 14. Encrypt File with system generated symmetric key
+ Mode:		
+ Input Type:		File
+ API:	
  ```javascript
  FileEncrypt("noKey");
  ```
+ Call:		
  ```javascript  
  - FileEncrypt("noKey");
  ```
+ Output:		
  ```json
  {"data":"{\"Key\":\"D8JyUnuGq3veHiDF/h0dbbmTquNwVzs5NCaBIXI3pMU=\",\"File\":\"IAAAABTgY+rxOzaIuwWMTxvaQFaEXfaWx35TISpCCuhm5wFL0U4HrY8hD5fISUQaGGpt5DFxj/hPWEqDwzakC3oZPZc=\",\"FileName\":\"cot-test.txt\"}","OP":"FileEncrypt"}
  ```
## 15. Encrypt File with user provided symmetric key
+ Mode:		
+ Input Type:		File
+ API:	
  ```javascript
  FileEncrypt(symKey);
  ```
+ Example:		
  ```javascript
  FileEncrypt(document.getElementById('file-input').value);
  FileEncrypt( ‘D8JyUnuGq3veHiDF/h0dbbmTquNwVzs5NCaBIXI3pMU=’);
  ```
+ Output:		
  ```
  {"data":"{\"Key\":\"D8JyUnuGq3veHiDF/h0dbbmTquNwVzs5NCaBIXI3pMU=\",\"File\":\"IAAAAHaakewtGGKz/JQiAgBcbyS+JNGWIPhmUbYiyweZEw2s+6Wue33zmpdEJS1frp0iuMWuqFbmEP3kHhVK+UZIRwU=\",\"FileName\":\"cot-test.txt\"}","OP":"FileEncrypt"}
  ```

## 16. Decrypt File 
+ Mode:		
+ Input Type:	File
+ API:
  ```javascript
  FileDecrypt(jsonData);
  ```
+ Example:
  ```javascript
  FileDecrypt(document.getElementById('file-output').value);
  FileDecrypt(‘{"Key":"D8JyUnuGq3veHiDF/h0dbbmTquNwVzs5NCaBIXI3pMU=","File":"IAAAAHbWf6h9lOWL4fiv7AM/uDdeno7gcIBUU/XV9aLJmqV1RWAG37+rf0XBkAn11W9iEFV9gviNPmoW3OFKXbHLbDU=","FileName":"cot-test.txt"}’);
  ```
+ Output:		
  ```json
  {"data":"cot-test.txt Decrypted","OP":"FileDecrypt"}
  ```

## 17. Base64 Encode
+ API:	
  ```javascript
  Base64Encode(data);
  ```
+ Example:
  ```javascript
  Base64Encode(document.getElementById('input-oper').value);
  Base64Encode(‘example text to encode BASE64’);
  ```
+ Output:		
  ```json
  {"data":"ZXhhbXBsZSB0ZXh0IHRvIGVuY29kZSBCQVNFNjQ=","OP":"Base64Encode"}
  ```

## 18. Base64 Decode
+ API:	
  ```javascript
  Base64Decode(data);
  ```
+ Example:
  ```javascript
  Base64Decode(document.getElementById('output-oper').value);
  Base64Decode( ‘ZXhhbXBsZSB0ZXh0IHRvIGVuY29kZSBCQVNFNjQ=’ );
  ```
+ Output:		
  ```json
  {"data":"example text to encode BASE64","OP":"Base64Decode"}
  ```

## 19. Generate Symmetric Key and IV for AES
+ API:	
  ```javascript
  GetSymmetricKey();
  ```
+ Call:	
  ```javascript
  GetSymmetricKey();
  ```
+ Output:
  ```json
  {"data":"{\"Key\":\"IUWjwBY3/hZGtMZrZQwRUAvby7/7lu/lMIsOgl6rGeQ=\",\"IV\":\"I6FcbibH5VK7UfLJUY8z+w==\",\"PlainText\":null,\"CypherText\":null}","OP":"GetSymmetricKey"}
  ```
