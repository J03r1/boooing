# Mini-level — Inleveren

**Naam:** Joeri
**Klas:** SD1A
**Datum:**  06-11-26
**Les:** GDV Les 6

---

## Wat heb ik gemaakt?
ik heb een lava parkour level gemaakt waar je moet jumpen naar de finish
...

---

## Screenshot / GIF van je level


[main/doooing.gif]([https://drive.google.com/file/d/1ymz8nA8TT3sfyw0s22gh1afBLibjwcXL/view?usp=drive_link](https://youtu.be/XAzBopCmiKg))
klik



---

## Bewegend object
mijn player met een vector 3 en getkeydown...


...

```csharp


```
void Update()
{
        float horizontal = Input.GetAxis("Horizontal");
        float vertical = Input.GetAxis("Vertical");

        Vector3 direction = new Vector3(horizontal, 0f, vertical);

        rb.linearVelocity = new Vector3(
            direction.x * speed,
            rb.linearVelocity.y,
            direction.z * speed
            );
        if (Input.GetKeyDown(KeyCode.Space) && IsGrounded == true)
        {
            jump();
}
---

## Collider of trigger

finish 
...

```csharp
```
 private void OnCollisionEnter(Collision collision)
 {
     if (collision.gameObject.CompareTag("Finish"))
     { Debug.Log("YOU WON CONGRATULATIONS"); }
         if (collision.gameObject.CompareTag("floor"))
     {
         IsGrounded = true;
     }
---

## Logica met `if` of `switch`

de finish en de jumps laten zorgen

...

```csharp


```
if ()
{
 if (Input.GetKeyDown(KeyCode.Space) && IsGrounded == true)
 {
     jump();
     IsGrounded = false;
     Debug.Log("Doooing  ");
 }
}
---

## Eigen extra idee
jumpen boven lava en de text van BOOOING als je jumpt



...

```csharp


```
 if (Input.GetKeyDown(KeyCode.Space) && IsGrounded == true)
 {
     jump();
     IsGrounded = false;
     Debug.Log("Doooing  ");
 }
---

## Evaluatie

### Wat ging goed? en waarom?

het lukte met een klein beetje hulp prima

...

### Wat vond je lastig? en waarom?

even herhalen voor mijzelf hoe je jump werkte
was dit vergeten

...

### Wat zou je een volgende keer anders doen?
niks

...
