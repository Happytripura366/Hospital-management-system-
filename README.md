Hospital Management System:
class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

class Patient extends Person {
    String patientId;
    Treatment treatment;

    public Patient(String name, int age, String patientId) {
        super(name, age);
        this.patientId = patientId;
    }

    public void assignTreatment(Treatment treatment) {
        this.treatment = treatment;
        System.out.println(name + " assigned to treatment: " + treatment.diagnosis);
    }
}

class Staff extends Person {
    String staffId;
    String role;

    public Staff(String name, int age, String staffId, String role) {
        super(name, age);
        this.staffId = staffId;
        this.role = role;
    }
}

class Treatment {
    String diagnosis;
    String medication;

    public Treatment(String diagnosis, String medication) {
        this.diagnosis = diagnosis;
        this.medication = medication;
    }

    public void prescribe() {
        System.out.println("Prescribed medication: " + medication + " for " + diagnosis);
    }
}# Hospital-management-system-
