# Smart-Pulse-Rate-Monitoring-System
This project simulates a health monitoring embedded system that measures and analyzes a person's pulse rate. It checks if the heart rate is normal, low or high and provides an alert message if the pulse is outside safe limits.
#include <stdio.h>

int main() {
    int pulseRate; // Beats per minute (BPM)
    
    printf("---- SMART PULSE RATE MONITORING SYSTEM ----\n");
    printf("Enter current pulse rate (in BPM): ");
    scanf("%d", &pulseRate);

    printf("\nAnalyzing Heart Condition...\n");

    if (pulseRate < 60) {
        printf("⚠️ Alert: Low Pulse Rate (%d BPM)\n", pulseRate);
        printf("Condition: Bradycardia detected! Increase physical activity or consult a doctor.\n");
    } 
    else if (pulseRate >= 60 && pulseRate <= 100) {
        printf("✅ Normal Pulse Rate: %d BPM\n", pulseRate);
        printf("Condition: Heart rate is healthy and normal.\n");
    } 
    else if (pulseRate > 100 && pulseRate <= 140) {
        printf("⚠️ Alert: High Pulse Rate (%d BPM)\n", pulseRate);
        printf("Condition: Mild Tachycardia. Take rest and stay hydrated.\n");
    } 
    else {
        printf("🚨 Critical Alert! Very High Pulse Rate: %d BPM\n", pulseRate);
        printf("Condition: Severe Tachycardia detected! Immediate medical attention required.\n");
    }

    printf("\nSystem Monitoring Complete.\n");
    return 0;
}
